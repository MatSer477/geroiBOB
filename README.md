async function findPortrait(img, fullName, note, status, wrap) {
  const person = plainName(fullName);
  const parts = person.split(/\s+/);
  const surname = parts[0] || "";
  const first = parts[1] || "";

  const norm = s =>
    (s || "").toLocaleLowerCase("ru").replace(/ё/g, "е");

  const isNameMatch = title =>
    norm(title).includes(norm(surname)) &&
    norm(title).includes(norm(first));

  // 1. Сначала пробуем найти фотографию в русской Википедии.
  try {
    const params = new URLSearchParams({
      action: "query",
      format: "json",
      formatversion: "2",
      list: "search",
      srsearch: person,
      srnamespace: "0",
      srlimit: "10",
      origin: "*"
    });

    const response = await fetch(
      "https://ru.wikipedia.org/w/api.php?" + params.toString()
    );

    if (response.ok) {
      const data = await response.json();
      const pages = data.query?.search || [];

      // Сначала проверяем статьи с совпадением имени,
      // а затем статьи, найденные по более широкому запросу.
      const orderedPages = [
        ...pages.filter(p => isNameMatch(p.title)),
        ...pages.filter(p => !isNameMatch(p.title))
      ];

      for (const found of orderedPages) {
        const imageParams = new URLSearchParams({
          action: "query",
          format: "json",
          formatversion: "2",
          prop: "pageimages",
          piprop: "thumbnail",
          pithumbsize: "700",
          titles: found.title,
          redirects: "1",
          origin: "*"
        });

        const imageResponse = await fetch(
          "https://ru.wikipedia.org/w/api.php?" +
          imageParams.toString()
        );

        if (!imageResponse.ok) continue;

        const imageData = await imageResponse.json();
        const page = (imageData.query?.pages || [])
          .find(p => p.thumbnail?.source);

        if (page) {
          img.src = page.thumbnail.source;
          note.textContent = isNameMatch(page.title)
            ? "Фото из русской Википедии"
            : "Возможное фото из найденной статьи";

          status.textContent =
            "Источник: статья «" + page.title +
            "». Проверьте, действительно ли на фото этот человек.";

          img.onerror = () => {
            img.remove();
            note.textContent = "Ищем другое изображение";
            status.textContent =
              "Не удалось загрузить фото. Откройте архивную ссылку ниже.";
          };

          return;
        }
      }
    }
  } catch (error) {
    // Если Википедия не ответила, переходим к Wikimedia Commons.
  }

  // 2. Ищем в архиве изображений Wikimedia Commons.
  // Допускаются неточные совпадения.
  const queries = [
    person,
    surname + " " + first,
    surname + " орден Славы",
    surname + " Великая Отечественная война",
    person + " СССР",
    "солдаты Красной армии Великая Отечественная война",
    "полные кавалеры ордена Славы Саратовская область"
  ];

  const seen = new Set();

  for (const query of queries) {
    try {
      const params = new URLSearchParams({
        action: "query",
        generator: "search",
        gsrnamespace: "6",
        gsrsearch: query,
        gsrlimit: "30",
        prop: "imageinfo",
        iiprop: "url",
        iiurlwidth: "700",
        format: "json",
        formatversion: "2",
        origin: "*"
      });

      const response = await fetch(
        "https://commons.wikimedia.org/w/api.php?" +
        params.toString()
      );

      if (!response.ok) continue;

      const data = await response.json();
      const pages = data.query?.pages || [];

      const usable = pages.filter(page =>
        page.imageinfo?.[0] &&
        (page.imageinfo[0].thumburl || page.imageinfo[0].url) &&
        !seen.has(page.title)
      );

      // Если есть совпадение по имени — выбираем его.
      // Если нет — берём первое доступное фото по запросу.
      const match =
        usable.find(page => isNameMatch(page.title)) ||
        usable[0];

      if (!match) continue;

      seen.add(match.title);

      const info = match.imageinfo[0];
      img.src = info.thumburl || info.url;

      const exactMatch = isNameMatch(match.title);

      note.textContent = exactMatch
        ? "Возможное фото героя"
        : "Фото из исторического архива";

      status.textContent =
        "Источник: " +
        match.title.replace(/^File:/, "") +
        ". " +
        (exactMatch
          ? "Совпадение по имени не гарантирует личность на снимке."
          : "Это неточное совпадение: изображение может быть не связано с героем.") +
        " Проверьте описание оригинала.";

      img.onerror = () => {
        img.remove();
        note.textContent = "Фото не загрузилось";
        status.textContent =
          "Попробуйте открыть архивный поиск по ссылке ниже.";
      };

      return;
    } catch (error) {
      // Пробуем следующий поисковый запрос.
    }
  }

  // 3. Если автоматический поиск не дал результата.
  img.remove();
  note.textContent = "Фото не найдено автоматически";
  status.textContent =
    "Попробуйте открыть архивный поиск по ссылке ниже.";
}
