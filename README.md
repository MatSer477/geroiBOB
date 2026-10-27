
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Портреты и биографии героев Великой Отечественной войны, связанных с Саратовом и Саратовской областью.">
<title>Герои ВОВ | Саратовская область</title>

<style>
:root {
    --green: #243e30;
    --green2: #365944;
    --gold: #d7b66c;
    --paper: #f5f1e8;
    --white: #fff;
    --text: #292f29;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
}

body {
    font-family: Arial, sans-serif;
    background: var(--paper);
    color: var(--text);
    line-height: 1.7;
}

header {
    background: var(--green);
    color: white;
    padding: 18px 6%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
}

.logo {
    font-size: 22px;
    font-weight: bold;
    color: var(--gold);
}

nav {
    display: flex;
    flex-wrap: wrap;
    gap: 18px;
}

nav a {
    color: white;
    text-decoration: none;
}

nav a:hover {
    color: var(--gold);
}

.hero {
    padding: 90px 7%;
    color: white;
    background: linear-gradient(125deg, #14271c, #4b6750);
}

.hero-inner {
    max-width: 900px;
}

.hero-label {
    color: var(--gold);
    font-weight: bold;
    letter-spacing: 2px;
    text-transform: uppercase;
}

.hero h1 {
    font-size: clamp(36px, 6vw, 62px);
    line-height: 1.15;
    margin: 22px 0;
}

.hero p {
    font-size: 18px;
    max-width: 760px;
    margin-bottom: 28px;
}

.button {
    display: inline-block;
    background: var(--gold);
    color: #1e3024;
    border: none;
    border-radius: 5px;
    padding: 12px 20px;
    text-decoration: none;
    font-weight: bold;
    cursor: pointer;
    font-size: 15px;
}

.button:hover {
    background: #f2dfac;
}

section {
    padding: 60px 7%;
}

.section-title {
    font-size: 34px;
    color: var(--green);
    margin-bottom: 12px;
}

.line {
    width: 70px;
    height: 4px;
    background: var(--gold);
    margin: 18px 0 25px;
}

.intro {
    background: white;
}

.intro p {
    max-width: 900px;
}

.intro-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 30px;
}

.intro-card {
    padding: 22px;
    background: var(--paper);
    border-left: 4px solid var(--gold);
}

.intro-card h3 {
    color: var(--green);
    margin-bottom: 8px;
}

.heroes-section {
    background: #eae5d9;
}

.description {
    color: #62665f;
    max-width: 850px;
    margin-bottom: 25px;
}

.search-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 30px;
}

.search {
    width: 100%;
    max-width: 480px;
    padding: 14px;
    border: 1px solid #c6c0b3;
    border-radius: 5px;
    background: white;
    font-size: 16px;
}

.count {
    margin-bottom: 20px;
    color: #686b62;
}

.heroes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
    gap: 25px;
}

.hero-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 5px 18px #00000012;
    display: flex;
    flex-direction: column;
    transition: transform .2s;
}

.hero-card:hover {
    transform: translateY(-4px);
}

.photo-wrap {
    height: 300px;
    background: #ded9cc;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}

.photo-wrap img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    padding: 8px;
}

.photo-placeholder {
    display: none;
    width: 100%;
    height: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
    color: var(--green);
    padding: 20px;
    background: linear-gradient(145deg, #ded9cc, #c8c2b2);
}

.photo-placeholder span {
    font-size: 64px;
    margin-bottom: 10px;
}

.card-content {
    padding: 22px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex: 1;
}

.tag {
    color: #7a612d;
    background: #f5edd8;
    font-size: 12px;
    font-weight: bold;
    padding: 4px 9px;
    margin-bottom: 12px;
    border-radius: 3px;
}

.hero-card h3 {
    color: var(--green);
    font-size: 23px;
    line-height: 1.35;
    margin-bottom: 8px;
}

.years {
    font-weight: bold;
    color: #777;
    margin-bottom: 12px;
}

.card-content > p {
    margin-bottom: 15px;
}

.card-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: auto;
    padding-top: 12px;
}

.secondary {
    background: var(--green);
    color: white;
}

.secondary:hover {
    background: var(--green2);
}

.biography {
    display: none;
    border-top: 1px solid #ddd8cc;
    margin-top: 18px;
    padding-top: 16px;
    width: 100%;
}

.biography.open {
    display: block;
}

.biography p {
    margin-bottom: 13px;
}

.source-link {
    color: #315b41;
    overflow-wrap: anywhere;
}

.no-results {
    display: none;
    padding: 25px 0;
}

.history {
    background: white;
}

.history-item {
    border-left: 3px solid var(--gold);
    padding: 0 0 25px 22px;
    margin: 25px 0;
}

.history-item h3 {
    color: var(--green);
    margin-bottom: 5px;
}

.memory {
    background: var(--green);
    color: white;
    text-align: center;
}

.memory h2 {
    color: var(--gold);
}

.memory blockquote {
    max-width: 750px;
    margin: 20px auto;
    font-size: 25px;
    font-style: italic;
}

.memory p {
    max-width: 750px;
    margin: auto;
}

footer {
    background: #17261d;
    color: #ddd;
    text-align: center;
    padding: 30px 6%;
}

footer a {
    color: var(--gold);
}

footer p + p {
    margin-top: 8px;
    font-size: 14px;
}

@media (max-width: 600px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    nav {
        gap: 12px;
    }

    section {
        padding: 42px 5%;
    }

    .hero {
        padding: 65px 5%;
    }

    .section-title {
        font-size: 28px;
    }

    .photo-wrap {
        height: 270px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">★ Память поколений</div>
    <nav>
        <a href="#about">О проекте</a>
        <a href="#heroes">Герои</a>
        <a href="#history">История</a>
        <a href="#memory">Память</a>
    </nav>
</header>

<main>

<section class="hero">
    <div class="hero-inner">
        <div class="hero-label">1941–1945 · Саратовский край</div>
        <h1>Герои Великой Отечественной войны</h1>
        <div class="line"></div>
        <p>
            Портреты, биографии и подвиги людей, которые сражались
            за свободу Родины. Сохраняем память о героях,
            чьи судьбы связаны с Саратовом и Саратовской областью.
        </p>
        <a class="button" href="#heroes">Познакомиться с героями</a>
    </div>
</section>

<section class="intro" id="about">
    <h2 class="section-title">О проекте</h2>
    <div class="line"></div>
    <p>
        Саратовская земля связана с судьбами многих участников
        Великой Отечественной войны. Одни родились в Саратове
        и районах области, другие учились, работали или проходили
        военную подготовку на нашей земле.
    </p>
    <p style="margin-top:14px">
        На этой странице размещены биографические карточки,
        а также ссылки на архивный источник для проверки
        и дальнейшего изучения истории.
    </p>

    <div class="intro-grid">
        <div class="intro-card">
            <h3>Фотографии</h3>
            <p>Портреты героев. Если внешний адрес изображения недоступен, карточка покажет аккуратную заглушку.</p>
        </div>
        <div class="intro-card">
            <h3>Биографии</h3>
            <p>Истории жизни, военная служба и подвиги защитников Родины.</p>
        </div>
        <div class="intro-card">
            <h3>Поиск</h3>
            <p>Найди нужную карточку по имени, фамилии или месту рождения.</p>
        </div>
    </div>
</section>

<section class="heroes-section" id="heroes">
    <h2 class="section-title">Герои и их биографии</h2>
    <div class="line"></div>
    <p class="description">
        Нажми «Читать биографию», чтобы открыть подробности.
        Для проверки сведений используй ссылку на архивный источник.
    </p>

    <div class="search-row">
        <input
            class="search"
            id="search"
            type="search"
            placeholder="Поиск по имени или фамилии..."
            aria-label="Поиск героев"
        >
    </div>

    <p class="count" id="count">Героев на странице: 4</p>

    <div class="heroes-grid" id="heroesGrid">

        <article class="hero-card" data-search="алексей петрович маресьев камышин летчик авиация">
            <div class="photo-wrap">
                <img
                    src="https://commons.wikimedia.org/wiki/Special:FilePath/Маресьев,_Алексей_Петрович_001.png"
                    alt="Портрет Алексея Петровича Маресьева"
                    loading="lazy"
                    onerror="this.style.display='none';this.nextElementSibling.style.display='flex';"
                >
                <div class="photo-placeholder">
                    <span>★</span>
                    <b>Алексей Петрович Маресьев</b>
                    <small>Портрет временно недоступен</small>
                </div>
            </div>
            <div class="card-content">
                <span class="tag">Герой Советского Союза</span>
                <h3>Алексей Петрович Маресьев</h3>
                <div class="years">1916–2001</div>
                <p>Лётчик-истребитель, уроженец Камышина, пример мужества и невероятной силы воли.</p>
                <div class="card-actions">
                    <button class="button" onclick="toggleBiography(this)" aria-expanded="false">Читать биографию</button>
                    <a class="button secondary" href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">Архив</a>
                </div>
                <div class="biography">
                    <p>
                        Алексей Маресьев родился 20 мая 1916 года
                        в Камышине Саратовской губернии. Он мечтал
                        стать лётчиком и впоследствии окончил
                        военное авиационное училище.
                    </p>
                    <p>
                        В апреле 1942 года во время боевого вылета
                        его самолёт был подбит. Получив тяжёлые
                        ранения, он добирался к своим через лес.
                        В результате повреждений ему ампутировали
                        обе ноги.
                    </p>
                    <p>
                        Маресьев освоил протезы, восстановил
                        лётные навыки и вернулся в боевую авиацию.
                        В 1943 году ему присвоили звание Героя
                        Советского Союза.
                    </p>
                    <p>
                        Его судьба стала основой книги Бориса
                        Полевого «Повесть о настоящем человеке».
                    </p>
                    <p class="source-link">
                        Источник для дальнейшей проверки:
                        <a class="source-link" href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">сайт саратовских героев</a>.
                    </p>
                </div>
            </div>
        </article>

        <article class="hero-card" data-search="виктор васильевич талалихин тепловка вольский район летчик">
            <div class="photo-wrap">
                <img
                    src="https://commons.wikimedia.org/wiki/Special:FilePath/Victor_Talalihkin.jpg"
                    alt="Портрет Виктора Васильевича Талалихина"
                    loading="lazy"
                    onerror="this.style.display='none';this.nextElementSibling.style.display='flex';"
                >
                <div class="photo-placeholder">
                    <span>★</span>
                    <b>Виктор Васильевич Талалихин</b>
                    <small>Портрет временно недоступен</small>
                </div>
            </div>
            <div class="card-content">
                <span class="tag">Герой Советского Союза</span>
                <h3>Виктор Васильевич Талалихин</h3>
                <div class="years">1918–1941</div>
                <p>Военный лётчик, прославившийся воздушным тараном во время обороны Москвы.</p>
                <div class="card-actions">
                    <button class="button" onclick="toggleBiography(this)" aria-expanded="false">Читать биографию</button>
                    <a class="button secondary" href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">Архив</a>
                </div>
                <div class="biography">
                    <p>
                        Виктор Талалихин родился 18 сентября 1918 года
                        в селе Тепловка Саратовской губернии.
                        Он занимался в аэроклубе, затем окончил
                        авиационное училище и стал военным лётчиком.
                    </p>
                    <p>
                        В ночь на 7 августа 1941 года Талалихин
                        совершил ночной воздушный таран немецкого
                        бомбардировщика над Москвой. Он покинул
                        повреждённый самолёт с парашютом и выжил.
                    </p>
                    <p>
                        8 августа 1941 года ему присвоили звание
                        Героя Советского Союза. Виктор Талалихин
                        погиб в воздушном бою 27 октября 1941 года.
                    </p>
                    <p class="source-link">
                        Источник для дальнейшей проверки:
                        <a class="source-link" href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">сайт саратовских героев</a>.
                    </p>
                </div>
            </div>
        </article>

        <article class="hero-card" data-search="николай михайлович скоморохов лапоть летчик истребитель">
            <div class="photo-wrap">
                <img
                    src="https://commons.wikimedia.org/wiki/Special:FilePath/Nikolai_Skomorokhov.jpg"
                    alt="Портрет Николая Михайловича Скоморохова"
                    loading="lazy"
                    onerror="this.style.display='none';this.nextElementSibling.style.display='flex';"
                >
                <div class="photo-placeholder">
                    <span>★</span>
                    <b>Николай Михайлович Скоморохов</b>
                    <small>Портрет временно недоступен</small>
                </div>
            </div>
            <div class="card-content">
                <span class="tag">Дважды Герой Советского Союза</span>
                <h3>Николай Михайлович Скоморохов</h3>
                <div class="years">1920–1994</div>
                <p>Советский лётчик-истребитель, участник многочисленных воздушных боёв.</p>
                <div class="card-actions">
                    <button class="button" onclick="toggleBiography(this)" aria-expanded="false">Читать биографию</button>
                    <a class="button secondary" href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">Архив</a>
                </div>
                <div class="biography">
                    <p>
                        Николай Скоморохов родился в 1920 году
                        в Саратовской губернии. Он стал лётчиком
                        истребительной авиации и участвовал в
                        боевых действиях на фронте.
                    </p>
                    <p>
                        В ходе войны он проявил себя как опытный
                        пилот, участвовал во многих воздушных боях
                        и получил высокие государственные награды.
                    </p>
                    <p>
                        Скоморохов был дважды удостоен звания
                        Героя Советского Союза. После войны
                        продолжил службу и занимался подготовкой
                        военных кадров.
                    </p>
                    <p class="source-link">
                        Дополнительные сведения:
                        <a class="source-link" href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">сайт саратовских героев</a>.
                    </p>
                </div>
            </div>
        </article>

        <article class="hero-card" data-search="федор дмитриевич глухов александров гай сержант пулеметчик">
            <div class="photo-wrap">
                <img
                    src="https://commons.wikimedia.org/wiki/Special:FilePath/Fedor_Glukhov.jpg"
                    alt="Портрет Фёдора Дмитриевича Глухова"
                    loading="lazy"
                    onerror="this.style.display='none';this.nextElementSibling.style.display='flex';"
                >
                <div class="photo-placeholder">
                    <span>★</span>
                    <b>Фёдор Дмитриевич Глухов</b>
                    <small>Портрет временно недоступен</small>
                </div>
            </div>
            <div class="card-content">
                <span class="tag">Герой Советского Союза</span>
                <h3>Фёдор Дмитриевич Глухов</h3>
                <div class="years">1906–1943</div>
                <p>Гвардии сержант, командир пулемётного расчёта, уроженец Александрова Гая.</p>
                <div class="card-actions">
                    <button class="button" onclick="toggleBiography(this)" aria-expanded="false">Читать биографию</button>
                    <a class="button secondary" href="https://saratov-geroi.ru/stats_prosm.php?ist=9&ur=1" target="_blank" rel="noopener">Архив</a>
                </div>
                <div class="biography">
                    <p>
                        Фёдор Дмитриевич Глухов родился в 1906 году
                        в селе Александров Гай Саратовской области.
                        Он служил в Красной армии и участвовал
                        в боях Великой Отечественной войны.
                    </p>
                    <p>
                        Глухов был гвардии сержантом и командиром
                        пулемётного расчёта 184-го гвардейского
                        стрелкового полка 62-й гвардейской
                        стрелковой дивизии.
                    </p>
                    <p>
                        Он погиб 6 октября 1943 года.
                        В архивном каталоге Саратовской области
                        он представлен среди Героев Советского Союза.
                    </p>
                    <p class="source-link">
                        Архивная категория:
                        <a class="source-link" href="https://saratov-geroi.ru/stats_prosm.php?ist=9&ur=1" target="_blank" rel="noopener">уроженцы Саратовской области</a>.
                    </p>
                </div>
            </div>
        </article>

    </div>

    <p class="no-results" id="noResults">По вашему запросу героев не найдено.</p>

    <p class="description" style="margin-top:30px">
        Это начальная подборка, а не полный список архива. Биографии
        и изображения следует сверять с архивными записями перед
        публикацией исторического проекта.
    </p>
</section>

<section class="history" id="history">
    <h2 class="section-title">Саратовская область в годы войны</h2>
    <div class="line"></div>

    <div class="history-item">
        <h3>1941 год — начало войны</h3>
        <p>
            Жители региона уходили на фронт, предприятия
            перестраивались на военные нужды, а город принимал
            эвакуированных и помогал армии.
        </p>
    </div>

    <div class="history-item">
        <h3>1942–1943 годы — помощь фронту</h3>
        <p>
            Саратов был важным тыловым центром. Здесь работали
            госпитали, производились необходимые фронту товары,
            оказывалась помощь раненым.
        </p>
    </div>

    <div class="history-item">
        <h3>9 мая 1945 года — Великая Победа</h3>
        <p>
            Победа стала результатом мужества фронтовиков,
            самоотверженности тружеников тыла и усилий всего народа.
        </p>
    </div>
</section>

<section class="memory" id="memory">
    <h2>Никто не забыт, ничто не забыто</h2>
    <blockquote>
        «Память о героях живёт, пока мы рассказываем их истории».
    </blockquote>
    <p>
        Изучай историю своей области, береги семейные архивы
        и передавай память о защитниках Родины следующим поколениям.
    </p>
</section>

</main>

<footer>
    <p>Память поколений — Саратов и Саратовская область</p>
    <p>
        Архивный источник:
        <a href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">
            saratov-geroi.ru
        </a>
    </p>
    <p>Учебный исторический проект</p>
</footer>

<script>
function toggleBiography(button) {
    const biography = button
        .closest(".card-content")
        .querySelector(".biography");

    const isOpen = biography.classList.toggle("open");

    button.textContent = isOpen
        ? "Скрыть биографию"
        : "Читать биографию";

    button.setAttribute("aria-expanded", String(isOpen));
}

const searchInput = document.getElementById("search");
const cards = Array.from(document.querySelectorAll(".hero-card"));
const noResults = document.getElementById("noResults");
const count = document.getElementById("count");

function searchHeroes() {
    const query = searchInput.value
        .trim()
        .toLocaleLowerCase("ru");

    let visible = 0;

    cards.forEach(card => {
        const text = (
            card.dataset.search + " " + card.innerText
        ).toLocaleLowerCase("ru");

        const matches = text.includes(query);

        card.style.display = matches ? "flex" : "none";

        if (matches) visible++;
    });

    noResults.style.display = visible ? "none" : "block";
    count.textContent = "Найдено героев: " + visible;
}

searchInput.addEventListener("input", searchHeroes);
</script>

</body>
</html>
