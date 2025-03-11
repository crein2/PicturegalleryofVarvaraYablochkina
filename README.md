<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Картинная галерея</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #000;
            color: #fff;
            line-height: 1.6;
        }

        header {
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
        }

        header h1 {
            font-size: 2.5rem;
            margin: 0;
        }

        header p {
            font-style: italic;
            font-size: 1.2rem;
            margin-top: 10px;
        }

        .about-art {
            max-width: 800px;
            margin: 40px auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(255, 255, 255, 0.1);
        }

        .about-art h2 {
            text-align: center;
            color: #2575fc;
        }

        .about-art p {
            text-align: justify;
            font-size: 1rem;
            line-height: 1.8;
        }

        .quote {
            text-align: center;
            padding: 40px 20px;
            font-style: italic;
            font-size: 1.2rem;
            color: #ccc;
            background: rgba(255, 255, 255, 0.05);
            margin: 20px 0;
            border-left: 5px solid #2575fc;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 10px;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 2rem;
            color: white;
            cursor: pointer;
        }

        footer {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            color: #ccc;
            font-size: 0.9rem;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 2rem;
            }

            .gallery {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Картинная галерея</h1>
        <p>"Искусство — это лежащая в основе всего творчество." — Пабло Пикассо</p>
    </header>

    <div class="about-art">
        <h2>О цифровом искусстве и информационной эстетике</h2>
        <p>
            Информационное искусство — это направление современного искусства, которое использует технологии, данные и цифровые инструменты для создания произведений. Оно возникло на стыке искусства, науки и технологий и стало отражением эпохи, в которой мы живем.
        </p>
        <p>
            Цифровое искусство позволяет художникам экспериментировать с новыми формами выражения. Например, использование алгоритмов, искусственного интеллекта и больших данных открывает новые горизонты для творчества. Произведения могут быть интерактивными, динамическими и даже автономными, что делает их уникальными.
        </p>
        <p>
            Одним из ключевых аспектов информационного искусства является его способность визуализировать сложные данные. Художники создают работы, которые помогают людям лучше понять мир вокруг них, будь то климатические изменения, социальные сети или экономические процессы. Это искусство не только украшает пространство, но и заставляет задуматься.
        </p>
        <p>
            Как сказал Эдвард Туфте, эксперт по визуализации данных: "Хорошая графика — это не просто красивая картинка, это способ передать информацию так, чтобы она была понятна и полезна." В этом смысле информационное искусство становится мостом между наукой и эстетикой.
        </p>
    </div>

    <div class="quote">
        "Каждый художник был сначала любителем." — Ральф Уолдо Эмерсон
    </div>

    <div class="gallery">
        <!-- Изображение 1 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+1')">
            <img src="https://avatars.mds.yandex.net/i?id=a09f0cfe840e7961c73f506b850b7d6b_l-5233156-images-thumbs&n=13"Цифровое искусство 1">
        </div>
        <!-- Изображение 2 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+2')">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+2" alt="Цифровое искусство 2">
        </div>
        <!-- Изображение 3 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+3')">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+3" alt="Цифровое искусство 3">
        </div>
        <!-- Изображение 4 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+4')">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+4" alt="Цифровое искусство 4">
        </div>
        <!-- Изображение 5 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+5')">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+5" alt="Цифровое искусство 5">
        </div>
        <!-- Изображение 6 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+6')">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+6" alt="Цифровое искусство 6">
        </div>
        <!-- Изображение 7 -->
        <div class="gallery-item" onclick="openModal('https://via.placeholder.com/1200x800?text=Цифровое+искусство+7')">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+7" alt="Цифровое искусство 7">
        </div>
    </div>

    <div class="quote">
        "Искусство — это не то, что вы видите, а то, что вы заставляете других увидеть." — Эдгар Дега
    </div>

    <footer>
        &copy; 2025 Картинная галерея. Все права защищены.
    </footer>

    <!-- Модальное окно -->
    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img id="modalImage" src="" alt="Увеличенное изображение">
    </div>

    <script>
        function openModal(imageSrc) {
            const modal = document.getElementById('modal');
            const modalImage = document.getElementById('modalImage');
            modal.style.display = 'flex';
            modalImage.src = imageSrc;
        }

        function closeModal() {
            const modal = document.getElementById('modal');
            modal.style.display = 'none';
        }
    </script>
</body>
</html>
