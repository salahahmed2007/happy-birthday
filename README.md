
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Countdown ❤️</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            min-height: 100vh;
            font-family: Arial, sans-serif;
            overflow-x: hidden;
            background: linear-gradient(135deg, #160006, #4b0010, #120006);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* الخلفية */
        body::before {
            content: "";
            position: fixed;
            inset: 0;
            background:
                radial-gradient(circle at 50% 30%, rgba(255, 40, 90, 0.25), transparent 35%),
                radial-gradient(circle at 20% 80%, rgba(255, 0, 80, 0.15), transparent 30%);
            pointer-events: none;
        }

        .container {
            width: min(900px, 92%);
            text-align: center;
            padding: 35px 20px;
            position: relative;
            z-index: 5;
        }

        .title {
            font-size: clamp(35px, 7vw, 70px);
            margin-bottom: 10px;
            text-shadow: 0 0 15px #ff174d, 0 0 35px #ff174d;
            animation: pulse 2s infinite;
        }

        .subtitle {
            font-size: 18px;
            opacity: 0.85;
            margin-bottom: 35px;
        }

        /* العداد */
        .countdown {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            margin-bottom: 40px;
        }

        .time-box {
            background: rgba(255, 255, 255, 0.09);
            border: 1px solid rgba(255, 100, 130, 0.35);
            border-radius: 20px;
            padding: 20px 10px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 35px rgba(0, 0, 0, 0.3);
        }

        .number {
            display: block;
            font-size: clamp(35px, 7vw, 65px);
            font-weight: bold;
            color: #ff4770;
            text-shadow: 0 0 15px rgba(255, 40, 90, 0.8);
        }

        .label {
            display: block;
            margin-top: 5px;
            color: #ffd5df;
            font-size: 15px;
        }

        /* المكانين */
        .messages {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 15px;
        }

        .message-box {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 100, 130, 0.3);
            border-radius: 20px;
            padding: 20px;
            backdrop-filter: blur(8px);
        }

        .message-box h2 {
            font-size: 20px;
            margin-bottom: 12px;
            color: #ff7895;
        }

        textarea {
            width: 100%;
            min-height: 120px;
            resize: vertical;
            border: none;
            outline: none;
            border-radius: 14px;
            padding: 15px;
            font-size: 16px;
            font-family: Arial, sans-serif;
            background: rgba(0, 0, 0, 0.35);
            color: white;
        }

        textarea::placeholder {
            color: #d8aeb8;
        }

        /* العناصر النازلة */
        .falling {
            position: fixed;
            top: -80px;
            pointer-events: none;
            z-index: 2;
            animation-name: fall;
            animation-timing-function: linear;
            animation-fill-mode: forwards;
        }

        .heart {
            color: #ff416c;
            font-size: 25px;
            filter: drop-shadow(0 0 8px rgba(255, 40, 90, 0.8));
        }

        .balloon {
            width: 28px;
            height: 36px;
            border-radius: 50% 50% 45% 45%;
            background: #ff4770;
            position: relative;
            box-shadow: 0 0 12px rgba(255, 70, 110, 0.6);
        }

        .balloon::after {
            content: "";
            position: absolute;
            width: 1px;
            height: 45px;
            background: rgba(255,255,255,0.6);
            left: 50%;
            top: 35px;
        }

        .balloon::before {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            border-left: 5px solid transparent;
            border-right: 5px solid transparent;
            border-top: 7px solid #ff4770;
        }

        @keyframes fall {
            0% {
                transform: translateY(-100px) rotate(0deg);
                opacity: 0;
            }

            10% {
                opacity: 1;
            }

            100% {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0.8;
            }
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }

            50% {
                transform: scale(1.03);
            }
        }

        /* الموبايل */
        @media (max-width: 650px) {
            .countdown {
                grid-template-columns: repeat(2, 1fr);
            }

            .messages {
                grid-template-columns: 1fr;
            }

            .container {
                padding-top: 50px;
                padding-bottom: 50px;
            }

            .subtitle {
                font-size: 15px;
            }
        }
    </style>
</head>

<body>

    <div class="container">

        <h1 class="title">❤️ 10/2 ❤️</h1>

        <p class="subtitle">
            
        </p>

        <div class="countdown">

            <div class="time-box">
                <span class="number" id="days">00</span>
                <span class="label">يوم</span>
            </div>

            <div class="time-box">
                <span class="number" id="hours">00</span>
                <span class="label">ساعة</span>
            </div>

            <div class="time-box">
                <span class="number" id="minutes">00</span>
                <span class="label">دقيقة</span>
            </div>

            <div class="time-box">
                <span class="number" id="seconds">00</span>
                <span class="label">ثانية</span>
            </div>

        </div>

        <div class="messages">

            <div class="message-box">
                <h2>the first</h2>
                <textarea placeholder="Wishing you all the best—happy birthday in advance."></textarea>
            </div>

            <div class="message-box">
                <h2>🎈 </h2>
                <textarea placeholder="I don't send congratulations; I program them."></textarea>
            </div>

        </div>

    </div>
    

    <script>
        // تاريخ الهدف: 2 أكتوبر 2026 الساعة 00:00
        const targetDate = new Date("October 2, 2026 00:00:00").getTime();

        function updateCountdown() {

            const now = new Date().getTime();
            const difference = targetDate - now;

            if (difference <= 0) {
                document.getElementById("days").textContent = "00";
                document.getElementById("hours").textContent = "00";
                document.getElementById("minutes").textContent = "00";
                document.getElementById("seconds").textContent = "00";

                document.querySelector(".subtitle").textContent =
                    "❤️ وصلنا لليوم المنتظر ❤️";

                return;
            }

            const days = Math.floor(difference / (1000 * 60 * 60 * 24));
            const hours = Math.floor(
                (difference / (1000 * 60 * 60)) % 24
            );
            const minutes = Math.floor(
                (difference / (1000 * 60)) % 60
            );
            const seconds = Math.floor(
                (difference / 1000) % 60
            );

            document.getElementById("days").textContent =
                String(days).padStart(2, "0");

            document.getElementById("hours").textContent =
                String(hours).padStart(2, "0");

            document.getElementById("minutes").textContent =
                String(minutes).padStart(2, "0");

            document.getElementById("seconds").textContent =
                String(seconds).padStart(2, "0");
        }

        updateCountdown();
        setInterval(updateCountdown, 1000);


        // إنشاء القلوب والبالونات
        function createFallingItem() {

            const item = document.createElement("div");

            item.classList.add("falling");

            const isHeart = Math.random() > 0.45;

            if (isHeart) {
                item.classList.add("heart");
                item.textContent = Math.random() > 0.5 ? "❤️" : "💗";
            } else {
                item.classList.add("balloon");
            }

            item.style.left = Math.random() * 100 + "vw";

            const duration = 5 + Math.random() * 7;
            item.style.animationDuration = duration + "s";

            const size = 0.7 + Math.random() * 0.8;
            item.style.transform = `scale(${size})`;

            document.body.appendChild(item);

            setTimeout(() => {
                item.remove();
            }, duration * 1000 + 1000);
        }

        // نزول العناصر باستمرار
        setInterval(createFallingItem, 350);

    </script>

</body>
</html>
