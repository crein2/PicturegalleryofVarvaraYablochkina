<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Картинная галерея</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }

        header {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 20px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        footer {
            text-align: center;
            padding: 10px;
            background: #2c3e50;
            color: white;
            margin-top: 20px;
        }

        @media (max-width: 600px) {
            .gallery {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Картинная галерея</h1>
        <p>7 изображений для вдохновения</p>
    </header>

    <div class="gallery">
        <!-- Изображение 1 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+1" alt="Изображение 1">
        
        <!-- Изображение 2 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+2" alt="Изображение 2">
        
        <!-- Изображение 3 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+3" alt="Изображение 3">
        
        <!-- Изображение 4 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+4" alt="Изображение 4">
        
        <!-- Изображение 5 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+5" alt="Изображение 5">
        
        <!-- Изображение 6 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+6" alt="Изображение 6">
        
        <!-- Изображение 7 -->
        <img src="https://via.placeholder.com/300x200?text=Фото+7" alt="Изображение 7">
    </div>

    <footer>
        <p>&copy; 2025 Картинная галерея</p>
    </footer>
</body>
</html>
