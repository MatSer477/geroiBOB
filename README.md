
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Герои ВОВ — Саратовская область</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:Arial,sans-serif;background:#f4f0e7;color:#26342b;line-height:1.65}
header{background:#193326;color:white;padding:18px 6%;display:flex;justify-content:space-between;align-items:center;gap:15px;flex-wrap:wrap}
.logo{font-size:21px;font-weight:bold;color:#e7c77e}
nav{display:flex;gap:16px;flex-wrap:wrap}
nav a{color:white;text-decoration:none}
nav a:hover{color:#e7c77e}
.hero{padding:80px 7%;background:linear-gradient(120deg,#172b20,#526a51);color:white}
.hero h1{font-size:clamp(34px,6vw,58px);line-height:1.2;max-width:850px;margin:20px 0}
.hero p{max-width:750px;margin-bottom:25px}
.btn{display:inline-block;background:#e7c77e;color:#1d2b20;padding:11px 18px;border:0;border-radius:5px;text-decoration:none;font-weight:bold;cursor:pointer}
.btn:hover{background:#f7e7b9}
section{padding:55px 7%}
h2{font-size:32px;color:#294737;margin-bottom:12px}
.intro{background:white}
.muted{color:#666;margin-bottom:25px;max-width:850px}
.search{width:100%;max-width:500px;padding:13px;border:1px solid #bbb;border-radius:5px;font-size:16px;margin:0 0 25px}
#heroes{background:#eae5d9}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:22px}
.card{background:white;border-radius:8px;overflow:hidden;box-shadow:0 4px 15px #00000012;display:flex;flex-direction:column}
.card img{width:100%;height:300px;object-fit:contain;background:#e5e0d5;padding:8px}
.content{padding:20px;display:flex;flex-direction:column;align-items:flex-start;flex:1}
.tag{font-size:12px;color:#826628;text-transform:uppercase;font-weight:bold;margin-bottom:8px}
.card h3{font-size:22px;line-height:1.3;color:#294737;margin-bottom:10px}
.content p{margin-bottom:12px}
.bio{display:none;border-top:1px solid #ddd;padding-top:14px;margin-top:8px}
.bio.open{display:block}
.content .btn{margin-top:auto}
.bio p{margin-bottom:12px}
.source{font-size:13px;margin-top:12px}
.source a{color:#315c42}
.history{background:white}
.history article{border-left:3px solid #d9b760;padding:0 0 22px 20px;margin:20px 0}
.history h3{color:#294737}
footer{background:#192c22;color:white;text-align:center;padding:30px 6%}
footer a{color:#e7c77e}
.empty{display:none;padding:20px}
@media(max-width:600px){header{align-items:flex-start;flex-direction:column}section{padding:40px 5%}.hero{padding:60px 5%}h2{font-size:27px}.card img{height:260px}}
</style>
</head>
<body>
<header>
 <div class="logo">★ Память поколений</div>
 <nav>
  <a href="#about">О проекте</a>
  <a href="#heroes">Герои</a>
  <a href="#history">История</a>
 </nav>
</header>

<main>
<section class="hero">
 <p>1941–1945 · Саратов и Саратовская область</p>
 <h1>Герои Великой Отечественной войны</h1>
 <p>Фотографии, биографии и истории подвигов людей, связанных с Саратовской землёй.</p>
 <a class="btn" href="#heroes">Смотреть героев</a>
</section>

<section class="intro" id="about">
 <h2>О проекте</h2>
 <p>Этот сайт посвящён памяти героев Великой Отечественной войны. Здесь собраны биографические справки о знаменитых лётчиках, защитниках Родины и уроженцах Саратовского края.</p>
 <p style="margin-top:12px">Архивный источник: <a href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">Саратовцы — герои Великой Отечественной войны</a>.</p>
</section>

<section id="heroes">
 <h2>Герои Саратовской области</h2>
 <p class="muted">Найди героя по имени или фамилии. Нажми «Читать биографию», чтобы открыть подробности.</p>
 <input class="search" id="search" type="search" placeholder="Поиск по имени..." aria-label="Поиск по имени героя">

 <div class="grid" id="grid">

  <article class="card" data-name="алексей маресьев камышин летчик">
   <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Маресьев,_Алексей_Петрович_001.png" alt="Алексей Маресьев" loading="lazy">
   <div class="content">
    <span class="tag">Герой Советского Союза</span>
    <h3>Алексей Петрович Маресьев</h3>
    <p><b>1916–2001</b></p>
    <p>Лётчик-истребитель, уроженец Камышина, ставший символом мужества и силы воли.</p>
    <button class="btn" onclick="toggleBio(this)" aria-expanded="false">Читать биографию</button>
    <div class="bio">
     <p>Алексей Маресьев родился 20 мая 1916 года в Камышине Саратовской губернии. Он окончил авиационное училище и во время Великой Отечественной войны служил лётчиком-истребителем.</p>
     <p>В апреле 1942 года его самолёт был сбит. Получив тяжёлые ранения ног, Маресьев пробирался к своим через лес. После ампутации обеих ног он научился ходить на протезах и добился возвращения в боевую авиацию.</p>
     <p>В августе 1943 года ему присвоили звание Героя Советского Союза. Его история стала основой «Повести о настоящем человеке» Бориса Полевого.</p>
     <p class="source">Источник и дополнительные материалы: <a href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">архив саратовских героев</a>.</p>
    </div>
   </div>
  </article>

  <article class="card" data-name="виктор талалихин тепловка летчик">
   <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Victor_Talalihkin.jpg" alt="Виктор Талалихин" loading="lazy">
   <div class="content">
    <span class="tag">Герой Советского Союза</span>
    <h3>Виктор Васильевич Талалихин</h3>
    <p><b>1918–1941</b></p>
    <p>Лётчик, прославившийся ночным воздушным тараном в небе над Москвой.</p>
    <button class="btn" onclick="toggleBio(this)" aria-expanded="false">Читать биографию</button>
    <div class="bio">
     <p>Виктор Талалихин родился 18 сентября 1918 года в селе Тепловка Саратовской губернии. Он окончил военную авиационную школу и участвовал в боевых действиях ещё до Великой Отечественной войны.</p>
     <p>В ночь на 7 августа 1941 года во время обороны Москвы он совершил ночной воздушный таран немецкого бомбардировщика и спасся с парашютом.</p>
     <p>8 августа 1941 года Талалихину было присвоено звание Героя Советского Союза. Он погиб в воздушном бою 27 октября 1941 года.</p>
     <p class="source">Источник и дополнительные материалы: <a href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">архив саратовских героев</a>.</p>
    </div>
   </div>
  </article>

  <article class="card" data-name="николай скоморохов лапоть летчик">
   <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Nikolai_Skomorokhov.jpg" alt="Николай Скоморохов" loading="lazy">
   <div class="content">
    <span class="tag">Дважды Герой Советского Союза</span>
    <h3>Николай Михайлович Скоморохов</h3>
    <p><b>1920–1994</b></p>
    <p>Советский лётчик-истребитель, участник многочисленных воздушных боёв.</p>
    <button class="btn" onclick="toggleBio(this)" aria-expanded="false">Читать биографию</button>
    <div class="bio">
     <p>Николай Скоморохов родился 19 мая 1920 года в селе Лапоть Саратовской губернии. В годы Великой Отечественной войны он стал лётчиком-истребителем и участвовал в боях на фронте.</p>
     <p>За боевые заслуги и личное мужество Скоморохов был дважды удостоен звания Героя Советского Союза. После войны он продолжил службу, занимался военным образованием и дослужился до высокого командного звания.</p>
     <p>Биографические детали и сведения о месте рождения следует сверять с архивной записью.</p>
     <p class="source">Архивный источник: <a href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">saratov-geroi.ru</a>.</p>
    </div>
   </div>
  </article>

 </div>
 <p id="empty" class="empty">Герои по такому запросу не найдены.</p>

 <div style="margin-top:30px">
  <h3>Продолжить поиск в архиве</h3>
  <p class="muted">В архиве есть и другие биографии. Открой исходный каталог в отдельной вкладке.</p>
  <a class="btn" href="https://saratov-geroi.ru/stats_prosm.php?ist=9&ur=1" target="_blank" rel="noopener">Открыть каталог героев региона</a>
 </div>
</section>

<section class="history" id="history">
 <h2>Память о войне</h2>
 <article>
  <h3>1941 год — начало войны</h3>
  <p>Жители Саратовской области уходили на фронт, предприятия перестраивались на военные нужды, в регионе принимали эвакуированных.</p>
 </article>
 <article>
  <h3>1942–1943 годы — помощь Сталинградскому фронту</h3>
  <p>Регион обеспечивал фронт транспортом, продовольствием и медицинской помощью. В Саратове работали госпитали.</p>
 </article>
 <article>
  <h3>9 мая 1945 года — Победа</h3>
  <p>Подвиг фронтовиков и тружеников тыла навсегда остался частью истории Саратовского края.</p>
 </article>
</section>
</main>

<footer>
 <p>Никто не забыт, ничто не забыто.</p>
 <p>Архивный источник: <a href="https://www.saratov-geroi.ru/" target="_blank" rel="noopener">saratov-geroi.ru</a></p>
</footer>

<script>
function toggleBio(button) {
    const bio = button.nextElementSibling;
    const isOpen = bio.classList.toggle("open");
    button.textContent = isOpen ? "Скрыть биографию" : "Читать биографию";
    button.setAttribute("aria-expanded", String(isOpen));
}

const search = document.getElementById("search");
const cards = [...document.querySelectorAll(".card")];
const empty = document.getElementById("empty");

search.addEventListener("input", function () {
    const query = this.value.trim().toLocaleLowerCase("ru");
    let visible = 0;

    cards.forEach(card => {
        const text = (
            card.dataset.name + " " + card.innerText
        ).toLocaleLowerCase("ru");

        const matches = text.includes(query);
        card.style.display = matches ? "flex" : "none";
        if (matches) visible++;
    });

    empty.style.display = visible ? "none" : "block";
});
</script>
</body>
</html>
