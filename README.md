<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday ❤️</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html,body{
    width:100%;
    min-height:100%;
}

body{
    min-height:100vh;
    overflow-x:hidden;
    font-family:Arial,Tahoma,sans-serif;
    color:white;
    background:
        radial-gradient(circle at 50% 15%,rgba(255,60,120,.16),transparent 30%),
        radial-gradient(circle at 20% 80%,rgba(255,0,70,.08),transparent 30%),
        linear-gradient(145deg,#160008,#35000f,#090003);
}

/* =========================
   نجوم الخلفية
========================= */

.stars{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:0;
    opacity:.7;
    background-image:
        radial-gradient(circle,rgba(255,255,255,.35) 1px,transparent 1px),
        radial-gradient(circle,rgba(255,100,150,.25) 1px,transparent 1px);
    background-size:90px 90px,140px 140px;
    background-position:10px 20px,50px 80px;
}

/* =========================
   المحتوى
========================= */

.main{
    position:relative;
    z-index:5;
    width:100%;
    max-width:1000px;
    margin:auto;
    padding:35px 20px 80px;
    text-align:center;
}

/* =========================
   العنوان
========================= */

.title{
    font-size:clamp(38px,6vw,72px);
    font-weight:900;
    margin-top:10px;
    color:#fff;
    text-shadow:
        0 0 10px #ff174f,
        0 0 25px #ff174f,
        0 0 50px rgba(255,23,79,.7);
    animation:titleGlow 2.5s ease-in-out infinite alternate;
}

.subtitle{
    margin-top:12px;
    font-size:18px;
    color:#ffd6df;
    line-height:1.8;
}

@keyframes titleGlow{
    from{
        text-shadow:
        0 0 8px #ff174f,
        0 0 20px #ff174f;
    }
    to{
        text-shadow:
        0 0 15px #ff174f,
        0 0 35px #ff174f,
        0 0 60px rgba(255,23,79,.8);
    }
}

/* =========================
   التورتة
========================= */

.cake-area{
    height:220px;
    display:flex;
    justify-content:center;
    align-items:flex-end;
    margin:5px 0 15px;
}

.cake{
    position:relative;
    width:150px;
    height:100px;
    border-radius:0 0 25px 25px;
    background:linear-gradient(
        to bottom,
        #ff9bb5 0%,
        #ff4f7d 45%,
        #d9154e 100%
    );
    box-shadow:
        0 15px 35px rgba(255,0,80,.3),
        inset 0 4px 10px rgba(255,255,255,.25);
    animation:cakeFloat 3s ease-in-out infinite;
}

.cake::before{
    content:"";
    position:absolute;
    width:165px;
    height:38px;
    left:-7.5px;
    top:-17px;
    border-radius:50%;
    background:#ffe5ed;
    box-shadow:
        0 5px 10px rgba(255,255,255,.2),
        inset 0 -5px 8px rgba(255,70,120,.18);
}

.cake::after{
    content:"";
    position:absolute;
    left:15px;
    right:15px;
    top:8px;
    height:15px;
    border-radius:50%;
    background:rgba(255,255,255,.45);
}

.candle{
    position:absolute;
    z-index:3;
    width:16px;
    height:60px;
    left:67px;
    top:-75px;
    border-radius:5px;
    background:
        repeating-linear-gradient(
            -45deg,
            #fff 0 8px,
            #ff416c 8px 16px
        );
    box-shadow:0 0 8px rgba(255,255,255,.3);
}

.flame{
    position:absolute;
    z-index:4;
    width:25px;
    height:35px;
    left:62.5px;
    top:-108px;
    background:linear-gradient(#fff4a0,#ff9d00,#ff3b00);
    border-radius:50% 50% 50% 50%;
    transform:rotate(45deg);
    box-shadow:
        0 0 15px #ff9d00,
        0 0 35px #ff5b00;
    animation:flame 0.8s ease-in-out infinite alternate;
}

@keyframes flame{
    from{
        transform:rotate(42deg) scale(.9);
    }
    to{
        transform:rotate(48deg) scale(1.1);
    }
}

@keyframes cakeFloat{
    0%,100%{
        transform:translateY(0);
    }
    50%{
        transform:translateY(-7px);
    }
}

/* =========================
   FLIP CLOCK
========================= */

.countdown{
    width:100%;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
    direction:rtl;
    margin-top:20px;
}

.time-box{
    text-align:center;
}

.flip-card{
    position:relative;
    height:105px;
    width:100%;
    border-radius:17px;
    overflow:hidden;

    background:
        linear-gradient(
            to bottom,
            rgba(35,0,12,.95),
            rgba(13,0,5,.98)
        );

    border:1px solid rgba(255,90,130,.22);

    box-shadow:
        0 10px 25px rgba(0,0,0,.45),
        inset 0 1px 0 rgba(255,255,255,.04);
}

.flip-card::after{
    content:"";
    position:absolute;
    z-index:10;
    top:50%;
    left:0;
    width:100%;
    height:2px;
    background:rgba(0,0,0,.75);
    box-shadow:
        0 1px 2px rgba(255,255,255,.04);
}


.number{
    position:absolute;
    inset:0;
    display:flex;
    justify-content:center;
    align-items:center;

    font-size:52px;
    font-weight:900;
    letter-spacing:2px;

    color:#ff547c;

    text-shadow:
        0 0 8px #ff315f,
        0 0 18px rgba(255,49,95,.8);
}

/* نص الوحدة */

.label{
    margin-top:12px;
    font-size:15px;
    font-weight:bold;
    color:#ffd4de;
}

.flip-card.flip{
    animation:cardGlow .6s ease;
}

.flip-card.flip .number{
    animation:numberFlip .65s cubic-bezier(.4,0,.2,1);
}

@keyframes numberFlip{
    0%{
        transform:perspective(500px) rotateX(0deg);
    }

    45%{
        transform:perspective(500px) rotateX(-90deg);
    }

    55%{
        transform:perspective(500px) rotateX(90deg);
    }

    100%{
        transform:perspective(500px) rotateX(0deg);
    }
}

@keyframes cardGlow{
    0%,100%{
        box-shadow:
            0 10px 25px rgba(0,0,0,.45),
            inset 0 1px 0 rgba(255,255,255,.04);
    }

    50%{
        box-shadow:
            0 10px 35px rgba(255,20,80,.18),
            inset 0 1px 0 rgba(255,255,255,.08);
    }
}



.messages{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:15px;
    margin-top:55px;
}

.message-box{
    padding:22px;
    border-radius:20px;

    background:rgba(255,255,255,.045);
    border:1px solid rgba(255,90,130,.2);

    box-shadow:
        0 10px 30px rgba(0,0,0,.25),
        inset 0 1px 0 rgba(255,255,255,.04);

    backdrop-filter:blur(8px);
}

.message-box h2{
    font-size:21px;
    margin-bottom:15px;
    color:#ff7f9e;
    text-shadow:0 0 10px rgba(255,50,100,.6);
}

textarea{
    width:100%;
    height:110px;
    resize:none;

    border:none;
    outline:none;

    border-radius:14px;
    padding:15px;

    background:rgba(10,0,5,.7);
    color:white;

    font-family:Arial,Tahoma,sans-serif;
    font-size:15px;

    border:1px solid rgba(255,80,120,.12);
}

textarea::placeholder{
    color:#a88790;
}


.music-button{
    margin-top:25px;

    border:none;
    outline:none;
    cursor:pointer;

    padding:16px 30px;
    border-radius:50px;

    color:white;
    background:linear-gradient(
        135deg,
        #ff315f,
        #d90045
    );

    font-size:17px;
    font-weight:bold;

    box-shadow:
        0 8px 25px rgba(255,0,70,.35);

    transition:.25s;
}

.music-button:hover{
    transform:translateY(-3px);
    box-shadow:
        0 12px 35px rgba(255,0,70,.5);
}

.music-button:active{
    transform:scale(.96);
}



.falling{
    position:fixed;
    top:-70px;
    z-index:2;
    pointer-events:none;
    user-select:none;

    animation:fall linear forwards;
}

.heart{
    font-size:28px;
    filter:
        drop-shadow(0 0 6px rgba(255,30,80,.8));
}

.balloon{
    width:30px;
    height:38px;

    border-radius:50% 50% 45% 45%;

    background:linear-gradient(
        135deg,
        #ff7596,
        #d90045
    );

    box-shadow:
        0 0 12px rgba(255,30,90,.4);
}

.balloon::after{
    content:"";
    position:absolute;

    width:1px;
    height:70px;

    background:rgba(255,255,255,.35);

    top:35px;
    left:50%;
}

@keyframes fall{
    0%{
        transform:translate3d(0,-70px,0) rotate(0deg);
        opacity:0;
    }

    10%{
        opacity:1;
    }

    50%{
        transform:translate3d(35px,50vh,0) rotate(12deg);
    }

    100%{
        transform:translate3d(-35px,115vh,0) rotate(-15deg);
        opacity:.15;
    }
}



@media(max-width:700px){

    .main{
        padding:25px 12px 60px;
    }

    .countdown{
        gap:8px;
    }

    .flip-card{
        height:82px;
        border-radius:13px;
    }

    .number{
        font-size:38px;
    }

    .label{
        font-size:12px;
        margin-top:9px;
    }

    .messages{
        grid-template-columns:1fr;
        margin-top:40px;
    }

    .cake-area{
        height:190px;
    }
}

@media(max-width:430px){

    .title{
        font-size:34px;
    }

    .subtitle{
        font-size:15px;
    }

    .flip-card{
        height:72px;
    }

    .number{
        font-size:31px;
    }

    .label{
        font-size:10px;
    }
}
</style>
</head>

<body>

<div class="stars"></div>

<main class="main">

 <h1 class="title">
        ❤️ Happy Birthday ❤️
    </h1>

  <p class="subtitle">
        <br>
        2 October 2026
    </p>

    <!-- التورتة -->
  <div class="cake-area">
        <div class="cake">
            <div class="candle"></div>
            <div class="flame"></div>
        </div>
    </div>

    <!-- الساعة -->
  <div class="countdown">
    <div class="time-box">
            <div class="flip-card" id="daysCard">
                <div class="number" id="days">00</div>
            </div>
            <div class="label">يوم</div>
        </div>

 <div class="time-box">
            <div class="flip-card" id="hoursCard">
                <div class="number" id="hours">00</div>
            </div>
            <div class="label">ساعة</div>
        </div>

  <div class="time-box">
            <div class="flip-card" id="minutesCard">
                <div class="number" id="minutes">00</div>
            </div>
            <div class="label">دقيقة</div>
        </div>

  <div class="time-box">
            <div class="flip-card" id="secondsCard">
                <div class="number" id="seconds">00</div>
            </div>
            <div class="label">ثانية</div>
        </div>

  </div>

  <div class="messages">

 <div class="message-box">
            <h2>1</h2>

 <textarea
                placeholder="Wishing you all the best—happy birthday in advance"
            ></textarea>
        </div>

 <div class="message-box">
            <h2>2</h2>

  <textarea
                placeholder="I don't send congratulations; I program them"
            ></textarea>
        </div>

  </div>

    <!-- الموسيقى -->
 <button class="music-button" id="musicBtn">
        🎵 تشغيل الموسيقى
    </button>

  <audio id="birthdayMusic" loop>
        <source
            src="https://www.youtube.com/shorts/OWKag_BKXJQ"
            type="audio/mpeg"
        >
    </audio>

</main>

<script>



const targetDate = new Date(
    2026,
    9,
    2,
    0,
    0,
    0
).getTime();


let oldValues = {
    days: "00",
    hours: "00",
    minutes: "00",
    seconds: "00"
};


function addFlip(cardId){

    const card = document.getElementById(cardId);

    card.classList.remove("flip");

    // إجبار المتصفح على إعادة تشغيل الأنيميشن
    void card.offsetWidth;

    card.classList.add("flip");
}


function updateCountdown(){

    const now = new Date().getTime();

    let distance = targetDate - now;

    if(distance <= 0){

        distance = 0;
    }


    const days = Math.floor(
        distance / (1000 * 60 * 60 * 24)
    );

    const hours = Math.floor(
        (distance / (1000 * 60 * 60)) % 24
    );

    const minutes = Math.floor(
        (distance / (1000 * 60)) % 60
    );

    const seconds = Math.floor(
        (distance / 1000) % 60
    );


    const values = {

        days: String(days).padStart(2,"0"),

        hours: String(hours).padStart(2,"0"),

        minutes: String(minutes).padStart(2,"0"),

        seconds: String(seconds).padStart(2,"0")

    };


    Object.keys(values).forEach(key => {

        const element = document.getElementById(key);

        if(values[key] !== oldValues[key]){

            element.textContent = values[key];

            addFlip(key + "Card");

            oldValues[key] = values[key];

        }

    });

}


updateCountdown();

setInterval(updateCountdown,1000);


/* =================================
   الموسيقى
================================= */

const music = document.getElementById("birthdayMusic");
const musicBtn = document.getElementById("musicBtn");


musicBtn.addEventListener("click", async () => {

    try{

        if(music.paused){

            await music.play();

            musicBtn.textContent = "⏸️ إيقاف الموسيقى";

        }else{

            music.pause();

            musicBtn.textContent = "🎵 تشغيل الموسيقى";

        }

    }catch(error){

        alert(
            "حط رابط MP3 مباشر للموسيقى الأول 🎵"
        );

    }

});


/* =================================
   القلوب والبالونات
================================= */

function createFallingItem(){

    const item = document.createElement("div");

    const isHeart = Math.random() > .45;

    item.classList.add("falling");

    if(isHeart){

        item.classList.add("heart");

        const hearts = [
            "❤️",
            "💗",
            "💖",
            "💓",
            "💕"
        ];

        item.textContent =
            hearts[
                Math.floor(Math.random()*hearts.length)
            ];

    }else{

        item.classList.add("balloon");

    }


    item.style.left =
        Math.random()*100 + "vw";


    const duration =
        7 + Math.random()*6;


    item.style.animationDuration =
        duration + "s";


    item.style.transform =
        `scale(${.7 + Math.random()*.7})`;


    document.body.appendChild(item);


    setTimeout(() => {

        item.remove();

    },(duration + 1)*1000);

}


setInterval(createFallingItem,650);


/* أول شوية عناصر */

for(let i=0;i<8;i++){

    setTimeout(
        createFallingItem,
        i*350
    );

}

</script>

</body>
</html>
