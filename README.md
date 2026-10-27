
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Герои ВОВ — Саратов и Саратовская область</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background: #f4f0e7;
    color: #26362c;
    line-height: 1.6;
}

header {
    background: #192c22;
    color: white;
    padding: 20px 7%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
}

.logo {
    color: #e6c57a;
    font-size: 21px;
    font-weight: bold;
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
    color: #e6c57a;
}

.hero {
    background: linear-gradient(135deg, #193426, #49644e);
    color: white;
    text-align: center;
    padding: 80px 20px;
}

.hero h1 {
    font-size: clamp(32px, 5vw, 55px);
    line-height: 1.2;
    margin: 20px auto;
    max-width: 900px;
}

.hero p {
    max-width: 750px;
    margin: 0 auto 25px;
    font-size: 18px;
}

.gold {
    color: #e6c57a;
}

.button {
    display: inline-block;
    background: #e6c57a;
    color: #203126;
    padding: 12px 22px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
    border: none;
    cursor: pointer;
}

.button:hover {
    background: white;
}

section {
    padding: 55px 7%;
}

h2 {
    font-size: 32px;
    margin-bottom: 15px;
    color: #294737;
}

.description {
    color: #62665f;
    margin-bottom: 25px;
    max-width: 850px;
}

.features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 30px;
}

.feature {
    background: white;
    padding: 25px;
    border-radius: 8px;
    border-bottom: 4px solid #d9b760;
}

.feature .symbol {
    font-size: 35px;
}

.feature h3 {
    margin: 10px 0;
}

.catalog {
    background: white;
}

.catalog-box {
    background: #f4f0e7;
    padding: 25px;
    border-radius: 8px;
    margin-bottom: 25px;
}

.catalog-links {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 20px;
}

.catalog-links a {
    background: #294737;
    color: white;
    padding: 10px 15px;
    border-radius: 4px;
    text-decoration: none;
}

.catalog-links a:hover {
    background: #42644e;
}

.frame-wrap {
    background: #e6e0d3;
    border-radius: 8px;
    padding: 10px;
}

iframe {
    width: 100%;
    height: 750px;
    border: none;
    background: white;
    border-radius: 5px;
}

.note {
    background: #fff4d8;
    padding: 18px;
    margin-top: 18px;
    border-left: 4px solid #d9b760;
    border-radius: 4px;
}

footer {
    background: #192c22;
    color: white;
    padding: 30px 7%;
    text-align: center;
}

footer a {
    color: #e6c57a;
}

@media(max-width: 600px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    nav {
        gap: 12px;
    }

    section {
        padding: 40px 6%;
    }

    iframe {
        height: 600px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">★ Память поколений</div>

    <nav>
        <a href="#about">О проекте</a>
        <a href="#catalog">Каталог героев</a>
        <a href="#memory">Наша память</a>
    </nav>
</header>

<main>

<section class="hero">
    <p class="gold">1941–1945 · Саратов и Саратовская область</p>

    <h1>Герои Великой Отечественной войны</h1>

    <p>
        Фотографии, биографии и истории подвигов людей,
        связанных с Саратовской землёй.
        Сохраним память о героях вместе.
    </p>

    <a class="button" href="#catalog">
        Перейти к каталогу
    </a>
</section>

<section id="about">
    <h2>О проекте</h2>

    <p>
        Этот сайт посвящён героям Великой Отечественной войны,
        уроженцам Саратова и Саратовской области, фронтовикам,
        ветеранам и труженикам тыла.
    </p>

    <div class="features">
        <div class="feature">
            <div class="symbol">📷</div>
            <h3>Фотографии</h3>
            <p>
                Портреты героев и исторические фотографии
                из опубликованных архивных материалов.
            </p>
        </div>

        <div class="feature">
            <div class="symbol">📖</div>
            <h3>Биографии</h3>
            <p>
                Истории жизни, военный путь, подвиги
                и награды защитников Родины.
            </p>
        </div>

        <div class="feature">
            <div class="symbol">🔎</div>
            <h3>Поиск</h3>
            <p>
                Переход к базе данных для поиска
                по имени, фамилии и другим сведениям.
            </p>
        </div>
    </div>
</section>

<section class="catalog" id="catalog">
    <h2>Каталог героев и Книга памяти</h2>

    <p class="description">
        Ниже находится попытка открыть исходный сайт
        «Саратовцы — герои Великой Отечественной войны».
        Через него можно перейти к биографиям, фотографиям
        и архивным сведениям.
    </p>

    <div class="catalog-box">
        <h3>Открыть оригинальную базу</h3>

        <p>
            Если каталог не отображается внутри страницы,
            открой его отдельно. Некоторые сайты запрещают
            встраивание в другие страницы.
        </p>

        <div class="catalog-links">
            <a href="https://www.saratov-geroi.ru/"
               target="_blank" rel="noopener noreferrer">
                Все разделы сайта
            </a>

            <a href="https://www.saratov-geroi.ru/pogib.php"
               target="_blank" rel="noopener noreferrer">
                Книга памяти
            </a>

            <a href="https://www.saratov-geroi.ru/arziya.php"
               target="_blank" rel="noopener noreferrer">
                Информация о проекте
            </a>
        </div>
    </div>

    <div class="frame-wrap">
        <iframe
            src="https://www.saratov-geroi.ru/"
            title="Каталог героев Саратовской области"
            loading="lazy"
            referrerpolicy="strict-origin-when-cross-origin">
        </iframe>
    </div>

    <div class="note">
        <strong>Важно:</strong>
        если вместо каталога появится пустое окно или сообщение
        об ошибке, нажми «Все разделы сайта» выше.
        Это ограничение исходного сайта, а не ошибка твоего HTML.
    </div>
</section>

<section id="memory">
    <h2>Никто не забыт, ничто не забыто</h2>

    <p>
        За каждой фамилией стоит человеческая судьба.
        Помнить о героях — значит сохранять историю своей семьи,
        своего города и своей страны для будущих поколений.
    </p>
</section>

</main>

<footer>
    <p>Память поколений — Саратов и Саратовская область</p>
    <p>
        Источник архивных материалов:
        <a href="https://www.saratov-geroi.ru/"
           target="_blank" rel="noopener noreferrer">
            saratov-geroi.ru
        </a>
    </p>
    <p>Учебный исторический проект</p>
</footer>

</body>
</html>
