[mogame.html](https://github.com/user-attachments/files/31256942/mogame.html)
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>مو گیمر | MO GAMER</title>

<style>
*{box-sizing:border-box}

html{scroll-behavior:smooth}

body{
    margin:0;
    background:#05050b;
    color:#fff;
    font-family:Tahoma,Arial,sans-serif;
}

/* HEADER */

header{
    position:sticky;
    top:0;
    z-index:50;
    background:rgba(5,5,11,.9);
    backdrop-filter:blur(15px);
    border-bottom:1px solid #29293d;
}

.nav{
    max-width:1300px;
    margin:auto;
    padding:15px 20px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:30px;
    font-weight:900;
    background:linear-gradient(90deg,#ff008c,#8b5cff,#00d9ff);
    -webkit-background-clip:text;
    color:transparent;
}

/* HERO */

.hero{
    min-height:430px;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:60px 20px;
    background:
      radial-gradient(circle at 15% 20%,rgba(255,0,140,.25),transparent 30%),
      radial-gradient(circle at 85% 30%,rgba(0,210,255,.22),transparent 30%);
}

.hero h1{
    margin:0;
    font-size:clamp(55px,10vw,110px);
    font-weight:1000;
    background:linear-gradient(90deg,#ff008c,#9b5cff,#00d9ff);
    -webkit-background-clip:text;
    color:transparent;
}

.hero p{
    max-width:750px;
    color:#aaaabd;
    line-height:2;
    font-size:18px;
}

/* SEARCH */

.search{
    width:min(700px,95%);
    display:flex;
    padding:7px;
    background:#11111d;
    border:1px solid #34344d;
    border-radius:18px;
}

.search input{
    flex:1;
    background:none;
    border:0;
    outline:0;
    color:white;
    padding:14px;
    font-size:16px;
}

.search button{
    border:0;
    border-radius:13px;
    padding:0 25px;
    color:white;
    font-weight:bold;
    cursor:pointer;
    background:linear-gradient(90deg,#ff008c,#744cff);
}

/* X MASTER AD */

.xmaster-ad{
    max-width:1250px;
    margin:25px auto 45px;
    padding:35px;
    border-radius:25px;
    border:1px solid #773cff;
    background:
      radial-gradient(circle at 10% 50%,rgba(255,0,140,.25),transparent 35%),
      radial-gradient(circle at 90% 50%,rgba(0,210,255,.25),transparent 35%),
      #0d0d19;
    box-shadow:0 0 50px rgba(139,92,255,.18);
}

.ad-inner{
    display:flex;
    align-items:center;
    gap:25px;
}

.ad-logo{
    width:100px;
    height:100px;
    flex-shrink:0;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:25px;
    font-size:48px;
    background:linear-gradient(135deg,#ff008c,#744cff,#00d9ff);
    box-shadow:0 0 40px rgba(255,0,140,.3);
}

.ad-small{
    color:#00d9ff;
    font-size:12px;
    font-weight:bold;
    letter-spacing:2px;
}

.ad-inner h2{
    margin:8px 0;
    font-size:32px;
}

.ad-inner p{
    color:#aaaabd;
    line-height:1.8;
}

.socials{
    display:flex;
    flex-wrap:wrap;
    gap:9px;
}

.socials button{
    border:1px solid #38384f;
    background:#181827;
    color:white;
    padding:10px 15px;
    border-radius:11px;
    cursor:pointer;
    transition:.25s;
}

.socials button:hover{
    transform:translateY(-3px);
    border-color:#ff008c;
    background:linear-gradient(90deg,#ff008c,#704cff);
}

/* FILTERS */

.filters{
    max-width:1300px;
    margin:0 auto 25px;
    padding:0 20px;
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
    gap:10px;
}

.filter{
    border:1px solid #35354b;
    background:#11111d;
    color:#ddd;
    padding:11px 20px;
    border-radius:50px;
    cursor:pointer;
}

.filter.active,
.filter:hover{
    color:white;
    border-color:#ff008c;
    background:linear-gradient(90deg,#ff008c,#743cff);
}

/* COUNTER */

.counter{
    text-align:center;
    color:#777;
    margin:20px;
}

.counter strong{
    color:#00d9ff;
}

/* GALLERY */

.gallery{
    max-width:1300px;
    margin:auto;
    padding:0 20px 70px;
    display:grid;
    grid-template-columns:repeat(auto-fill,minmax(280px,1fr));
    gap:22px;
}

.card{
    background:#10101b;
    border:1px solid #29293d;
    border-radius:20px;
    overflow:hidden;
    transition:.3s;
}

.card:hover{
    transform:translateY(-7px);
    border-color:#8b5cff;
    box-shadow:0 15px 45px rgba(0,0,0,.5);
}

.card-img{
    height:220px;
    position:relative;
    overflow:hidden;
    cursor:pointer;
    background:#151521;
}

.card-img img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
    transition:.5s;
}

.card:hover img{
    transform:scale(1.08);
}

.badge{
    position:absolute;
    top:12px;
    right:12px;
    background:rgba(0,0,0,.75);
    padding:7px 11px;
    border-radius:50px;
    font-size:12px;
}

.card-body{
    padding:18px;
}

.card-body h3{
    margin:0 0 8px;
}

.card-body p{
    color:#9999ad;
    line-height:1.8;
    font-size:14px;
}

.tags{
    display:flex;
    flex-wrap:wrap;
    gap:6px;
}

.tag{
    background:#09202a;
    border:1px solid #124355;
    color:#bdefff;
    padding:5px 8px;
    border-radius:7px;
    font-size:11px;
}

.no-result{
    display:none;
    grid-column:1/-1;
    text-align:center;
    padding:70px;
    color:#888;
}

/* LIGHTBOX */

.lightbox{
    position:fixed;
    inset:0;
    z-index:100;
    background:rgba(0,0,0,.95);
    display:none;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.lightbox.show{
    display:flex;
}

.lightbox img{
    max-width:90vw;
    max-height:80vh;
    border-radius:15px;
    box-shadow:0 0 70px #000;
}

.light-title{
    text-align:center;
    margin-top:15px;
    font-size:20px;
}

.close,
.prev,
.next{
    position:fixed;
    border:0;
    border-radius:50%;
    color:white;
    cursor:pointer;
}

.close{
    top:20px;
    left:20px;
    width:45px;
    height:45px;
    background:#ff1744;
    font-size:25px;
}

.prev,.next{
    top:50%;
    transform:translateY(-50%);
    width:55px;
    height:55px;
    background:#222232;
    font-size:25px;
}

.prev{right:25px}
.next{left:25px}

/* FOOTER */

footer{
    text-align:center;
    padding:40px;
    border-top:1px solid #20202d;
    color:#777;
}

/* MOBILE */

@media(max-width:650px){

    .ad-inner{
        flex-direction:column;
        text-align:center;
    }

    .socials{
        justify-content:center;
    }

    .xmaster-ad{
        margin:20px 15px 40px;
        padding:25px 18px;
    }

    .ad-inner h2{
        font-size:25px;
    }
}
</style>
</head>

<body>

<header>
<div class="nav">
    <div class="logo">🎮 مو گیمر</div>
</div>
</header>

<section class="hero">

<h1>مو گیمر</h1>

<p>
به گالری خفن‌ترین اتاق‌های گیمینگ،
ستاپ‌های RGB و سیستم‌های حرفه‌ای خوش آمدی 🔥
</p>

<div class="search">
<input
id="search"
type="text"
placeholder="جستجو: RGB، قرمز، آبی، چند مانیتوره..."
>
<button onclick="filterCards()">جستجو</button>
</div>

</section>


<!-- X MASTER AD -->

<section class="xmaster-ad">

<div class="ad-inner">

<div class="ad-logo">
🎮
</div>

<div>

<div class="ad-small">
SPECIAL GAMING CHANNEL
</div>

<h2>
🔥 ABOLFAZL X MASTER 🔥
</h2>

<p>
برای دیدن ویدیوهای گیمینگ،
سرگرمی، چالش و محتوای جذاب
صفحه‌های X Master را ببین!
</p>

<div class="socials">

<button onclick="social('youtube')">
▶ YouTube
</button>

<button onclick="social('instagram')">
📸 Instagram
</button>

<button onclick="social('aparat')">
▶ Aparat
</button>

<button onclick="social('telegram')">
✈️ Telegram
</button>

<button onclick="social('rubika')">
💬 Rubika
</button>

<button onclick="social('twitch')">
🎥 Twitch
</button>

<button onclick="social('discord')">
🎧 Discord
</button>

</div>

</div>
</div>

</section>


<!-- FILTERS -->

<div class="filters">

<button class="filter active"
onclick="setFilter('all',this)">
🎮 همه
</button>

<button class="filter"
onclick="setFilter('rgb',this)">
🌈 RGB
</button>

<button class="filter"
onclick="setFilter('red',this)">
🔴 قرمز
</button>

<button class="filter"
onclick="setFilter('blue',this)">
🔵 آبی
</button>

<button class="filter"
onclick="setFilter('triple',this)">
🖥️ چند مانیتوره
</button>

</div>


<div class="counter">
نمایش
<strong id="count">30</strong>
اتاق گیمینگ
</div>


<section class="gallery" id="gallery"></section>


<!-- LIGHTBOX -->

<div class="lightbox" id="lightbox">

<button class="close" onclick="closeLightbox()">×</button>

<button class="prev" onclick="previousImage()">❯</button>

<div>
<img id="lightboxImage" src="" alt="">
<div class="light-title" id="lightTitle"></div>
</div>

<button class="next" onclick="nextImage()">❮</button>

</div>


<footer>

🎮 مو گیمر — MO GAMER

<br><br>

ساخته شده برای عاشقان گیمینگ 🔥

</footer>


<script>

/* =========================
   X MASTER LINKS
========================= */

const socials = {

youtube:
"www.youtube.com/@AbolfazlXMaster84",

instagram:
"www.instagram.com/abolfazlxmaster84",

aparat:
"www.aparat.com/abolfazlxmaster",

telegram:
"t.me/ABOLFAZLXMASTER",

rubika:
"rubika.ir/abolfazlxmasterofficial",

twitch:
"m.twitch.tv/abolfazlxmaster/home",

discord:
"discord.gg/W4nGGk5Rfs"

};

function social(name){

    const link =
        "https://" + socials[name];

    window.open(link,"_blank");

}


/* =========================
   GAMING ROOMS
========================= */

const rooms = [

[
"Cyber RGB Setup",
"rgb blue triple",
"RGB • Blue • Triple",
"ستاپ حرفه‌ای چند مانیتوره",
"photo-1593305841991-05c297ba4575"
],

[
"Red Warrior",
"rgb red",
"Red • RGB",
"اتاق گیمینگ با نور قرمز",
"photo-1603481546238-487240415921"
],

[
"Blue Neon",
"rgb blue",
"Blue • Neon",
"نورپردازی آبی نئونی",
"photo-1616588589676-62b3bd4ff6d2"
],

[
"Triple Monitor",
"rgb triple",
"Triple • RGB",
"سه نمایشگر برای گیمر حرفه‌ای",
"photo-1547394765-185e1e68f34e"
],

[
"Red Beast",
"red",
"Red • PC",
"تم قرمز و مشکی",
"photo-1593640408182-31c70c8268f5"
],

[
"Ocean Setup",
"blue rgb",
"Blue • RGB",
"ستاپ آبی آرام",
"photo-1592840496694-26d035b52b48"
],

[
"RGB Station",
"rgb",
"RGB",
"ستاپ کاملاً رنگارنگ",
"photo-1618220179428-22790b461013"
],

[
"Red Command",
"red triple",
"Red • Triple",
"مرکز فرماندهی سه مانیتوره",
"photo-1598550476439-6847785fcea6"
],

[
"Blue Desk",
"blue",
"Blue",
"میز گیمینگ آبی",
"photo-1593642532400-2682810df593"
],

[
"Pro Arena",
"rgb triple",
"RGB • Triple",
"ستاپ مخصوص استریم",
"photo-1587202372775-e229f172b9d7"
],

[
"Red Zone",
"rgb red",
"Red • RGB",
"اتاق قرمز و مشکی",
"photo-1593642532973-d31b6557fa68"
],

[
"Neon Blue",
"blue rgb",
"Blue • Neon",
"فضای نئونی آبی",
"photo-1606144042614-b2417e99c4e3"
],

[
"RGB Machine",
"rgb",
"RGB",
"سیستم گیمینگ RGB",
"photo-1593305841991-05c297ba4575"
],

[
"Red Gamer",
"red",
"Red",
"اتاق گیمر قرمز",
"photo-1542751371-adc38448a05e"
],

[
"Blue Triple",
"blue triple",
"Blue • Triple",
"سه مانیتور با نور آبی",
"photo-1593642532842-98d0fd5ebc1a"
],

[
"Color Station",
"rgb",
"RGB",
"ستاپ رنگارنگ",
"photo-1612810436541-336d3b0c2f24"
],

[
"Red Triple",
"red triple",
"Red • Triple",
"سه نمایشگر قرمز",
"photo-1547394765-185e1e68f34e"
],

[
"Blue Room",
"blue rgb",
"Blue • RGB",
"اتاق آبی و بنفش",
"photo-1598550476439-6847785fcea6"
],

[
"Pro RGB",
"rgb triple",
"RGB • Triple",
"ستاپ حرفه‌ای",
"photo-1587202372162-5f5e1f8f0f7f"
],

[
"Fire Setup",
"red",
"Red",
"تم قرمز آتشین",
"photo-1560419015-7c427e8ae5ba"
],

[
"Blue Machine",
"blue",
"Blue",
"سیستم گیمینگ آبی",
"photo-1591488320449-011701bb6704"
],

[
"RGB Lab",
"rgb",
"RGB",
"آزمایشگاه RGB",
"photo-1603481546238-487240415921"
],

[
"Command Center",
"red triple",
"Red • Triple",
"مرکز فرماندهی گیمینگ",
"photo-1593640495253-23196b27a87f"
],

[
"Blue Gamer",
"blue rgb",
"Blue • RGB",
"ستاپ آبی مدرن",
"photo-1618220179428-22790b461013"
],

[
"Ultimate Room",
"rgb triple",
"RGB • Triple",
"اتاق کامل گیمینگ",
"photo-1547394765-185e1e68f34e"
],

[
"Red Core",
"red",
"Red • PC",
"ستاپ قرمز قدرتمند",
"photo-1587202372616-b43abea06c2a"
],

[
"Ocean Desk",
"blue",
"Blue",
"میز آبی مدرن",
"photo-1593642632823-8f785ba67e45"
],

[
"RGB Command",
"rgb triple",
"RGB • Triple",
"سه مانیتور RGB",
"photo-1593642532973-d31b6557fa68"
],

[
"Red Neon Room",
"red rgb",
"Red • RGB",
"اتاق نئونی قرمز",
"photo-1593305841991-05c297ba4575"
],

[
"Ultimate Gamer",
"blue rgb triple",
"Blue • RGB • Triple",
"ستاپ نهایی گیمر",
"photo-1606144042614-b2417e99c4e3"
]

];


/* =========================
   CREATE CARDS
========================= */

const gallery =
document.getElementById("gallery");

rooms.forEach((room,index)=>{

    const card =
    document.createElement("article");

    card.className="card";

    card.dataset.type=room[1];

    card.dataset.search=
        (
            room[0]+" "+
            room[1]+" "+
            room[2]+" "+
            room[3]
        ).toLowerCase();

    card.innerHTML=`

        <div class="card-img"
        onclick="openLightbox(${index})">

            <img
            src="https://images.unsplash.com/${room[4]}?auto=format&fit=crop&w=1200&q=85"
            alt="${room[0]}">

            <span class="badge">
                ${room[2]}
            </span>

        </div>

        <div class="card-body">

            <h3>${room[0]}</h3>

            <p>${room[3]}</p>

            <div class="tags">

                ${room[1].includes("rgb")
                ?'<span class="tag">RGB</span>':''}

                ${room[1].includes("red")
                ?'<span class="tag">Red</span>':''}

                ${room[1].includes("blue")
                ?'<span class="tag">Blue</span>':''}

                ${room[1].includes("triple")
                ?'<span class="tag">Triple Monitor</span>':''}

            </div>

        </div>
    `;

    gallery.appendChild(card);

});


const cards =
[...document.querySelectorAll(".card")];

const search =
document.getElementById("search");

const count =
document.getElementById("count");

let currentFilter="all";


/* =========================
   FILTER
========================= */

function setFilter(type,button){

    currentFilter=type;

    document
    .querySelectorAll(".filter")
    .forEach(x=>x.classList.remove("active"));

    button.classList.add("active");

    filterCards();
}


function filterCards(){

    const text=
        search.value.toLowerCase().trim();

    let visible=0;

    cards.forEach(card=>{

        const type=card.dataset.type;
        const words=card.dataset.search;

        const filterOK=
            currentFilter==="all" ||
            type.includes(currentFilter);

        const searchOK=
            !text ||
            words.includes(text);

        if(filterOK && searchOK){

            card.style.display="";

            visible++;

        }else{

            card.style.display="none";

        }

    });

    count.textContent=visible;

}


search.addEventListener(
    "input",
    filterCards
);


/* =========================
   LIGHTBOX
========================= */

let currentImage=0;

const lightbox=
document.getElementById("lightbox");

const lightImage=
document.getElementById("lightboxImage");

const lightTitle=
document.getElementById("lightTitle");


function openLightbox(index){

    currentImage=index;

    showImage();

    lightbox.classList.add("show");

}


function showImage(){

    const room=rooms[currentImage];

    lightImage.src=
        "https://images.unsplash.com/"+
        room[4]+
        "?auto=format&fit=crop&w=1600&q=90";

    lightImage.alt=room[0];

    lightTitle.textContent=
        room[0];

}


function closeLightbox(){

    lightbox.classList.remove("show");

}


function nextImage(){

    currentImage++;

    if(currentImage>=rooms.length)
        currentImage=0;

    showImage();

}


function previousImage(){

    currentImage--;

    if(currentImage<0)
        currentImage=rooms.length-1;

    showImage();

}


/* =========================
   KEYBOARD
========================= */

document.addEventListener(
"keydown",
e=>{

    if(!lightbox.classList.contains("show"))
        return;

    if(e.key==="Escape")
        closeLightbox();

    if(e.key==="ArrowLeft")
        nextImage();

    if(e.key==="ArrowRight")
        previousImage();

});


/* =========================
   CLICK OUTSIDE
========================= */

lightbox.addEventListener(
"click",
e=>{

    if(e.target===lightbox)
        closeLightbox();

});


/* =========================
   IMAGE FALLBACK
========================= */

document
.querySelectorAll(".card-img img")
.forEach(img=>{

    img.onerror=function(){

        this.src=
        "data:image/svg+xml;charset=UTF-8,"+
        encodeURIComponent(`
        <svg xmlns="http://www.w3.org/2000/svg"
        width="900" height="600">

        <rect width="100%"
        height="100%"
        fill="#11111d"/>

        <text x="50%" y="50%"
        fill="#ff008c"
        font-size="42"
        text-anchor="middle">

        MO GAMER

        </text>

        </svg>
        `);

    };

});

</script>

</body>
</html>
