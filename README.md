<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ROTIC - КОНЧЕНЫЙ МЕМ КОИН</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
            background: #ff00ff;
            color: #00ff00;
        }
        .crazy-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: repeating-linear-gradient(
                45deg,
                #ff00ff,
                #ff00ff 10px,
                #00ffff 10px,
                #00ffff 20px
            );
            z-index: -1;
            opacity: 0.3;
        }
        header {
            text-align: center;
            padding: 2rem;
            background: rgba(0, 0, 0, 0.7);
            margin-bottom: 2rem;
        }

        .logo {
            font-size: 5rem;
            font-weight: bold;
            color: #ffff00;
            text-shadow: 5px 5px 0 #ff0000;
            animation: rotate 5s infinite linear;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .slogan {
            font-size: 1.5rem;
            color: #ffffff;
        }

        .memes, .team {
            padding: 2rem;
            background: rgba(255, 255, 255, 0.2);
            margin: 1rem;
            border-radius: 20px;
            border: 3px dashed #00ff00;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
        }

        .meme-img {
            width: 300px;
            height: 300px;
            object-fit: cover;
            border: 5px solid #ff00ff;
            transition: transform 0.3s;
        }

        .meme-img:hover {
            transform: scale(1.1) rotate(10deg);
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .member {
            background: rgba(0, 0, 0, 0.5);
            padding: 1rem;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s;
        }

        .member:hover {
            transform: translateY(-10px);
            background: rgba(255, 0, 255, 0.7);
        }

        .member img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #00ffff;
        }

        .pulse {
            display: block;
            margin: 2rem auto;
            padding: 1rem 2rem;
            font-size: 1.5rem;
            background: #ff0000;
            color: #ffff00;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        footer {
            text-align: center;
            padding: 1rem;
            background: rgba(0, 0, 0, 0.7);
            margin-top: 2rem;
        }
    </style>
</head>
<body>
    <div class="crazy-bg"></div>
    
    <header>
        <h1 class="logo" id="roticLogo">ROTIC</h1>
        <p class="slogan">САМЫЙ КОНЧЕНЫЙ МЕМ КОИН !</p>
    </header>

    <main>
        <section class="memes">
            <h2>TRASH GALLERY </h2>
            <div class="gallery">
                <img src="https://cdn.leonardo.ai/users/63aecb9b-22c7-42f7-81ea-7610db42d1d5/generations/3254dfba-2889-4be7-af67-ae58e585f61c/Leonardo_Kino_XL_A_ridiculous_meme_coin_avatar_named_ROTIC_Sho_1.jpg" alt="Мем 1" class="meme-img">
                <img src="https://cdn.leonardo.ai/users/63aecb9b-22c7-42f7-81ea-7610db42d1d5/generations/dd234134-1c45-4434-9fd3-903732eca61b/Leonardo_Kino_XL_A_ridiculous_meme_coin_avatar_named_ROTIC_Sho_1.jpg" class="meme-img">
                <img src="https://cdn.leonardo.ai/users/63aecb9b-22c7-42f7-81ea-7610db42d1d5/generations/8dc5a324-62a7-4c7c-b80d-1fb2b9216d44/Leonardo_Kino_XL_A_ridiculous_meme_coin_avatar_named_ROTIC_Sho_1.jpg" alt="Мем 3" class="meme-img">
            </div>
        </section>

        <section class="team">
            <h2>КОМАНДА ДОЛБАЁБОВ</h2>
            <div class="team-grid">
                <div class="member">
                    <img src="https://i.imgur.com/3LWrumD.png" alt="Главный Дегенерат">
                    <h3>ГЛАВНЫЙ УЕБАН</h3>
                    <p>ПРОФЕССИОНАЛЬНО ПРОЕБЫВАЕТ ВСЕ </p>
                </div>
                <div class="member">
                    <img src="https://i.imgur.com/Ipmy2FR.jpeg" alt="РЕШАЛА">
                    <h3>РЕШАЛА - СУКА БОБЁР</h3>
                    <p>РЕШАЕТ ЛЮБЫЕ ВОПРОСЫ</p>
                </div>
                <div class="member">
                    <img src="https://i.imgur.com/ZzAVl72.png" alt="Маркетолог">
                    <h3>КАКОЙ-ТО ДЕГЕНЕРАТ</h3>
                    <p>НИКТО НЕ ЗНАЕТ , КТО ОН И ЧЕМ ОН ВООБЩЕ ЗАНЯТ, НО ОН ВРОДЕ КАК ТУТ РАБОТАЕТ</p>
                </div>
            </div>
        </section>

        <button id="buyButton" class="pulse">Купить ROTIC и потерять все!</button>
    </main>

    <footer>
        <p>© 2025 ROTIC🤡</p>
    </footer>

    <script>
        document.getElementById('buyButton').addEventListener('click', function() {
            alert('ПОЗДРАВЛЯЕМ! ВЫ ТОЛЬКО ЧТО ВСЕ ПРОЕБАЛИ ');
        });

        const logo = document.getElementById('roticLogo');
        let rotation = 0;
        
        setInterval(() => {
            rotation += 1;
            logo.style.transform = `rotate(${rotation}deg)`;
        }, 50);
    </script>
</body>
</html>
