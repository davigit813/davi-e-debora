<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="theme-color" content="#1a0a0f">
    <title>❤️ Davi & Debóra ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            width: 100%;
            height: 100%;
            overflow: hidden;
            background: #1a1a1a;
            font-family: 'Segoe UI', 'Poppins', system-ui, sans-serif;
            position: fixed;
            top: 0;
            left: 0;
        }

        .love-card {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: radial-gradient(circle at 30% 40%, #ff4d8f, #1a0a0f 80%);
            background-blend-mode: overlay;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            border: none;
            border-radius: 0;
            box-shadow: none;
        }

        .hearts-bg {
            position: absolute;
            inset: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
            opacity: 0.5;
            background-image: 
                radial-gradient(circle at 5% 10%, #ff99bb 2px, transparent 2px),
                radial-gradient(circle at 15% 85%, #ff99bb 3px, transparent 3px),
                radial-gradient(circle at 28% 42%, #ffb3c6 4px, transparent 4px),
                radial-gradient(circle at 45% 18%, #ff4d6d 3px, transparent 3px),
                radial-gradient(circle at 62% 73%, #ffb3c6 5px, transparent 5px),
                radial-gradient(circle at 80% 30%, #ff4d6d 3px, transparent 3px),
                radial-gradient(circle at 92% 65%, #ff99bb 4px, transparent 4px),
                radial-gradient(circle at 10% 55%, #ffb3c6 3px, transparent 3px),
                radial-gradient(circle at 50% 90%, #ff4d6d 5px, transparent 5px),
                radial-gradient(circle at 70% 10%, #ff99bb 4px, transparent 4px),
                radial-gradient(circle at 35% 70%, #ffb3c6 3px, transparent 3px),
                radial-gradient(circle at 88% 50%, #ff4d6d 4px, transparent 4px),
                radial-gradient(circle at 5% 95%, #ff99bb 3px, transparent 3px),
                radial-gradient(circle at 50% 5%, #ffb3c6 5px, transparent 5px),
                radial-gradient(circle at 20% 30%, #ff4d6d 4px, transparent 4px),
                radial-gradient(circle at 75% 85%, #ff99bb 3px, transparent 3px),
                radial-gradient(circle at 42% 50%, #ffb3c6 6px, transparent 6px),
                radial-gradient(circle at 60% 55%, #ff4d6d 4px, transparent 4px),
                radial-gradient(circle at 10% 20%, #ffb3c6 3px, transparent 3px),
                radial-gradient(circle at 90% 90%, #ff99bb 5px, transparent 5px);
            background-size: 120px 120px, 180px 180px, 220px 220px, 140px 140px, 200px 200px,
                160px 160px, 250px 250px, 190px 190px, 210px 210px, 170px 170px,
                150px 150px, 230px 230px, 100px 100px, 260px 260px, 130px 130px,
                180px 180px, 240px 240px, 110px 110px, 270px 270px, 190px 190px;
            background-repeat: repeat;
            background-position: 0 0;
            transform: scale(1.1);
            filter: drop-shadow(0 0 6px #ff3366aa);
        }

        .hearts-unicode {
            position: absolute;
            inset: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            opacity: 0.25;
            color: #ff99bb;
            font-size: 28px;
            line-height: 1.8;
            letter-spacing: 32px;
            word-break: break-all;
            display: flex;
            flex-wrap: wrap;
            align-content: space-around;
            justify-content: space-around;
            padding: 12px;
            text-shadow: 0 0 12px #ff3b7f, 0 0 30px #ff1a5e;
            font-family: 'Segoe UI Emoji', 'Apple Color Emoji', 'Noto Color Emoji', sans-serif;
        }
        .hearts-unicode span {
            display: inline-block;
            transform: rotate(5deg) scale(0.9);
            filter: drop-shadow(0 0 6px #ff77aa);
        }

        .center-box {
            position: relative;
            z-index: 10;
            background: #0d0d0d;
            background: linear-gradient(145deg, #1a0a0f, #0a0507);
            width: 82%;
            max-width: 480px;
            padding: 2.5rem 1.8rem;
            border-radius: 28px 8px 28px 8px;
            box-shadow: 0 0 0 2px #ff3b7f88, 0 20px 40px rgba(0, 0, 0, 0.9), 0 0 30px #ff1a5e55;
            border: 1px solid #ff6a9e55;
            text-align: center;
            backdrop-filter: blur(2px);
        }

        .center-box .nome-top {
            color: white;
            font-size: 2.8rem;
            font-weight: 800;
            letter-spacing: 4px;
            text-shadow: 0 0 30px #ff4d8f, 0 0 60px #ff1a5e;
            margin-bottom: 0.2rem;
            word-break: break-word;
        }

        .center-box h1 {
            color: white;
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 2px;
            text-shadow: 0 0 20px #ff3366, 0 0 40px #ff1a5e;
            margin-bottom: 0.2rem;
            word-break: break-word;
            line-height: 1.3;
        }

        /* FRASE "DESDE O DIA" - sem linha, só o texto */
        .center-box .subtitle {
            color: white;
            font-size: 1.8rem;
            font-weight: 600;
            letter-spacing: 3px;
            text-shadow: 0 0 20px #ff3366, 0 0 40px #ff1a5e;
            margin-bottom: 0.8rem;
            word-break: break-word;
        }

        .center-box .highlight-date {
            color: white;
            font-size: 3.2rem;
            font-weight: 800;
            background: #1a0a0f;
            padding: 0.2rem 0.8rem;
            border-radius: 40px;
            display: inline-block;
            letter-spacing: 4px;
            text-shadow: 0 0 20px #ff4d8f, 0 0 60px #ff1a5e;
            box-shadow: 0 0 0 2px #ff3b7f55, 0 0 20px #ff1a5e44;
            margin: 0.3rem 0 0.8rem 0;
            border: 1px solid #ff6a9e33;
        }

        .clock-container {
            margin-top: 1.2rem;
            display: flex;
            justify-content: center;
            gap: 0.4rem;
            flex-wrap: wrap;
            color: white;
            font-size: 1.8rem;
            font-weight: 600;
            letter-spacing: 2px;
            background: #0d0d0d;
            padding: 0.5rem 1.2rem;
            border-radius: 60px;
            border: 1px solid #ff3b7f44;
            box-shadow: 0 0 20px #ff1a5e22;
        }

        .clock-container .time-block {
            display: flex;
            gap: 0.2rem;
            align-items: center;
            background: #1a0a0f;
            padding: 0.2rem 0.7rem;
            border-radius: 40px;
            border-left: 2px solid #ff4d8f55;
            border-right: 2px solid #ff4d8f55;
        }

        .clock-container .time-block span {
            color: white;
            text-shadow: 0 0 20px #ff4d8f, 0 0 40px #ff1a5e;
            font-variant-numeric: tabular-nums;
        }

        .clock-container .separator {
            color: #ff6a9e;
            text-shadow: 0 0 10px #ff3366;
            font-weight: 300;
            padding: 0 0.1rem;
        }

        .clock-container .label {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            opacity: 0.7;
            margin-right: 4px;
            color: #ffb3c6;
        }

        @media (max-width: 550px) {
            .center-box { padding: 1.8rem 1.2rem; }
            .center-box .nome-top { font-size: 2.0rem; }
            .center-box h1 { font-size: 1.6rem; }
            .center-box .subtitle { font-size: 1.4rem; }
            .center-box .highlight-date { font-size: 2.4rem; padding: 0.1rem 0.6rem; }
            .clock-container { font-size: 1.3rem; padding: 0.3rem 0.6rem; gap: 0.2rem; }
            .clock-container .time-block { padding: 0.1rem 0.4rem; }
            .hearts-unicode { font-size: 20px; letter-spacing: 18px; line-height: 1.6; }
        }

        @media (max-width: 400px) {
            .center-box { padding: 1.2rem 0.8rem; width: 92%; }
            .center-box .nome-top { font-size: 1.6rem; }
            .center-box h1 { font-size: 1.3rem; }
            .center-box .subtitle { font-size: 1.1rem; }
            .center-box .highlight-date { font-size: 1.8rem; }
            .clock-container { font-size: 1rem; padding: 0.2rem 0.4rem; }
        }
    </style>
</head>
<body>
    <div class="love-card">
        <div class="hearts-bg"></div>
        <div class="hearts-unicode" aria-hidden="true">
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
            <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span> <span>❤️</span>
        </div>

        <div class="center-box">
            <div class="nome-top">DEBÓRA</div>
            <h1>EU TE AMO</h1>
            <div class="subtitle">DESDE O DIA</div>
            <div class="highlight-date">26/06/2026</div>
            <div class="clock-container" id="clockDisplay">
                <div class="time-block">
                    <span class="label">⏱️</span>
                    <span id="hours">00</span>
                </div>
                <span class="separator">:</span>
                <div class="time-block">
                    <span class="label">⏱️</span>
                    <span id="minutes">00</span>
                </div>
                <span class="separator">:</span>
                <div class="time-block">
                    <span class="label">⏱️</span>
                    <span id="seconds">00</span>
                </div>
            </div>
        </div>
    </div>

    <script>
        (function() {
            const STORAGE_KEY = 'amor_start_time';
            let startTime = localStorage.getItem(STORAGE_KEY);
            
            if (!startTime) {
                startTime = Date.now();
                localStorage.setItem(STORAGE_KEY, startTime);
            } else {
                startTime = parseInt(startTime, 10);
            }

            function updateClock() {
                const now = Date.now();
                const diff = now - startTime;
                const totalSeconds = Math.floor(diff / 1000);
                const hours = String(Math.floor(totalSeconds / 3600)).padStart(2, '0');
                const minutes = String(Math.floor((totalSeconds % 3600) / 60)).padStart(2, '0');
                const seconds = String(totalSeconds % 60).padStart(2, '0');

                document.getElementById('hours').textContent = hours;
                document.getElementById('minutes').textContent = minutes;
                document.getElementById('seconds').textContent = seconds;
            }

            updateClock();
            setInterval(updateClock, 1000);

            function entrarTelaCheia() {
                const el = document.documentElement;
                if (el.requestFullscreen) {
                    el.requestFullscreen().catch(() => {});
                } else if (el.webkitRequestFullscreen) {
                    el.webkitRequestFullscreen();
                } else if (el.msRequestFullscreen) {
                    el.msRequestFullscreen();
                }
            }

            window.addEventListener('load', function() {
                setTimeout(entrarTelaCheia, 300);
            });

            document.addEventListener('touchstart', function() {
                entrarTelaCheia();
            }, { once: true });

            document.addEventListener('click', function() {
                entrarTelaCheia();
            }, { once: true });

            document.addEventListener('touchstart', function() {
                if (!document.fullscreenElement && !document.webkitFullscreenElement) {
                    entrarTelaCheia();
                }
            });
        })();
    </script>
</body>
</html>
