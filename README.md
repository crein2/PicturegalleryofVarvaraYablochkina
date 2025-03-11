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
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
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
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Галерея с анимацией</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background: #f0f0f0;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
        }

        .gallery-item {
            cursor: pointer;
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            display: block;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        /* Модальное окно */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal-content {
            position: relative;
            max-width: 800px;
            max-height: 80vh;
            animation: zoomIn 0.5s ease;
        }

        .modal-img {
            width: 100%;
            height: auto;
            display: block;
        }

        .close {
            position: absolute;
            top: -20px;
            right: -20px;
            color: white;
            font-size: 30px;
            cursor: pointer;
            transition: color 0.3s;
        }

        .close:hover {
            color: #ff4444;
        }

        @keyframes zoomIn {
            from {
                transform: scale(0.8);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }
    </style>
</head>
<body>

<div class="gallery" id="gallery">
    <div class="gallery-item" data-src="image1.jpg">
        <img src="thumbnail1.jpg" alt="Изображение 1">
    </div>
    <div class="gallery-item" data-src="image2.jpg">
        <img src="thumbnail2.jpg" alt="Изображение 2">
    </div>
    <!-- Добавьте больше изображений -->
</div>

<div class="modal" id="modal">
    <span class="close">&times;</span>
    <img class="modal-img" id="modalImg">
</div>

<script>
    document.addEventListener('DOMContentLoaded', () => {
        const galleryItems = document.querySelectorAll('.gallery-item');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modalImg');
        const closeBtn = document.querySelector('.close');

        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                const src = item.getAttribute('data-src');
                modalImg.setAttribute('src', src);
                modal.style.display = 'flex';
                
                // Анимация появления
                setTimeout(() => {
                    modal.classList.add('active');
                }, 10);
            });
        });

        // Закрытие модального окна
        const closeModal = () => {
            modal.classList.remove('active');
            setTimeout(() => {
                modal.style.display = 'none';
            }, 500); // совпадает с длительностью анимации
        };

        closeBtn.addEventListener('click', closeModal);
        modal.addEventListener('click', (e) => {
            if (e.target === modal) closeModal();
        });
    });
</script>

</body>
</html>
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
        «Искусство есть микроскоп, который художник наводит на тайны души, чтобы показать эти общие для всех тайны людям» — Лев Толстой
    </div>

    <div class="gallery">
        <!-- Изображение 1 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+1" alt="Цифровое искусство 1">
        </div>
        <!-- Изображение 2 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+2" alt="Цифровое искусство 2">
        </div>
        <!-- Изображение 3 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+3" alt="Цифровое искусство 3">
        </div>
        <!-- Изображение 4 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+4" alt="Цифровое искусство 4">
        </div>
        <!-- Изображение 5 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+5" alt="Цифровое искусство 5">
        </div>
        <!-- Изображение 6 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+6" alt="Цифровое искусство 6">
        </div>
        <!-- Изображение 7 -->
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Цифровое+искусство+7" alt="Цифровое искусство 7">
        </div>
    </div>

    <div class="quote">
        «Искусство — выражение самых глубоких мыслей самым простым способом» — Альберт Эйнштейн.
    </div>

    <footer>
        &copy; 2025 Картинная галерея. Все права защищены.
    </footer>
</body>
</html>
