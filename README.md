<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Искусство Суши - Традиции и Современность</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0a192f;
            color: #e6f1ff;
            overflow-x: hidden;
        }
        
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            z-index: 380;
            background: rgba(10, 25, 47, 0.9);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            flex-direction: column;
        }
        
        .logo {
            font-size: 50px;
            font-weight: 700;
            color: #64ffda;
            text-decoration: none;
            letter-spacing: 2px;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: #ccd6f6;
            text-decoration: none;
            font-size: 16px;
            transition: color 0.3s ease;
            flex-direction: column;
        }
        
        .nav-links a:hover {
            color: #64ffda;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #64ffda;
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(10, 25, 47, 0.7), rgba(10, 25, 47, 0.9));
            z-index: -1;
        }
        
        .hero-content {
            text-align: center;
            z-index: 1;
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero h1 {
            font-size: 4.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #64ffda, #ccd6f6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: fadeInUp 1s ease;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 30px;
            color: #8892b0;
            animation: fadeInUp 1s ease 0.2s both;
        }
        
        .cta-button {
            display: inline-block;
            padding: 15px 30px;
            background: transparent;
            color: #64ffda;
            border: 1px solid #64ffda;
            border-radius: 4px;
            text-decoration: none;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease 0.4s both;
        }
        
        .cta-button:hover {
            background: rgba(100, 255, 218, 0.1);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(100, 255, 218, 0.2);
        }
        
        section {
            padding: 100px 50px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .section-title {
            font-size: 2.5rem;
            margin-bottom: 50px;
            text-align: center;
            color: #ccd6f6;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: #64ffda;
        }
        
        .history-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .history-text {
            font-size: 1.1rem;
            line-height: 1.6;
            color: #8892b0;
        }
        
        .history-image {
            position: relative;
            height: 400px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            background: linear-gradient(45deg, #1a1a2e, #16213e);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .sushi-types {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .sushi-card {
            background: rgba(23, 42, 69, 0.7);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            height: 400px;
        }
        
        .sushi-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 30px rgba(0, 0, 0, 0.4);
        }
        
        .sushi-image {
            height: 60%;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(45deg, #1a1a2e, #16213e);
        }
        
        .sushi-content {
            padding: 20px;
            height: 40%;
        }
        
        .sushi-title {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #64ffda;
        }
        
        .sushi-description {
            color: #8892b0;
            font-size: 0.9rem;
            line-height: 1.5;
        }
        
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 50px;
        }
        
        .gallery-item {
            height: 250px;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }
        
        .gallery-item:hover {
            transform: scale(1.05);
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(100, 255, 218, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: #64ffda;
        }
        
        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }
        
        .form-group label {
            color: #ccd6f6;
            font-size: 0.9rem;
        }
        
        .form-group input, 
        .form-group textarea {
            padding: 12px;
            background: rgba(23, 42, 69, 0.7);
            border: 1px solid #233554;
            border-radius: 4px;
            color: #ccd6f6;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }
        
        .form-group input:focus, 
        .form-group textarea:focus {
            outline: none;
            border-color: #64ffda;
        }
        
        .submit-btn {
            padding: 15px;
            background: transparent;
            color: #64ffda;
            border: 1px solid #64ffda;
            border-radius: 4px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            background: rgba(100, 255, 218, 0.1);
        }
        
        footer {
            padding: 30px 50px;
            text-align: center;
            background: rgba(23, 42, 69, 0.7);
            border-top: 1px solid #233554;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .social-links {
            display: flex;
            gap: 20px;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(100, 255, 218, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #64ffda;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background: #64ffda;
            color: #0a192f;
            transform: translateY(-3px);
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @media (max-width: 720px) {
            nav {
                padding: 15px 20px;
            }
            
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            section {
                padding: 80px 20px;
            }
            
            .history-content,
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 20px;
            }
        }
    </style>
</head>
<body>
    <nav>
        <a href="#" class="logo">SushiCom</a> 
            <div class="nav-links"><a href="#history">История</a><a href="#types">Виды суши</a><a href="#gallery">Галерея</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-bg"></div>
        <div class="hero-content">
            <h1>Искусство Суши</h1>
            <p>Погрузитесь в мир японской кухни, где каждая деталь имеет значение</p>
            <a href="#history" class="cta-button">Узнать больше</a>
        </div>
    </section>

    <section id="history">
        <h2 class="section-title">История Суши</h2>
        <div class="history-content">
            <div class="history-text">
                <p>Суши — это не просто блюдо, это целая философия, уходящая корнями в глубокую древность. Изначально суши представляли собой способ консервации рыбы в ферментированном рисе в Юго-Восточной Азии.</p>
                <p>В Японию эта техника попала примерно в VII-VIII веках и постепенно эволюционировала. К XIX веку появился стиль эдомаэ-дзуси, который считается прообразом современных суши.</p>
                <p>Сегодня суши — это всемирно признанное искусство, сочетающее в себе свежесть ингредиентов, мастерство приготовления и эстетическое наслаждение.</p>
            </div>
            <div class="history-image">
                <div style="color: #64ffda; font-size: 5rem;">🍣</div>
            </div>
        </div>
    </section>

    <section id="types">
        <h2 class="section-title">Виды Суши</h2>
        <div class="sushi-types">
            <!-- Нигири -->
            <div class="sushi-card">
                <div class="sushi-image">
                    <div style="color: #64ffda; font-size: 4rem;">🍙</div>
                </div>
                <div class="sushi-content">
                    <h3 class="sushi-title">Нигири</h3>
                    <p class="sushi-description">Классические суши, состоящие из овальной рисовой основы и кусочка рыбы или морепродуктов сверху.</p>
                </div>
            </div>
            
            <!-- Маки -->
            <div class="sushi-card">
                <div class="sushi-image">
                    <div style="color: #64ffda; font-size: 4rem;">🍥</div>
                </div>
                <div class="sushi-content">
                    <h3 class="sushi-title">Маки</h3>
                    <p class="sushi-description">Роллы, завернутые в нори с начинкой внутри. Бывают различных размеров и с разными комбинациями ингредиентов.</p>
                </div>
            </div>
            
            <!-- Сашими -->
            <div class="sushi-card">
                <div class="sushi-image">
                    <div style="color: #64ffda; font-size: 4rem;">🐟</div>
                </div>
                <div class="sushi-content">
                    <h3 class="sushi-title">Сашими</h3>
                    <p class="sushi-description">Тонко нарезанные ломтики свежей рыбы, подающиеся без риса. Идеально подходят для ценителей чистого вкуса.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="gallery">
        <h2 class="section-title">Галерея</h2>
        <div class="gallery">
            <div class="gallery-item" style="background: linear-gradient(45deg, #1abc9c, #3498db);">🍣</div>
            <div class="gallery-item" style="background: linear-gradient(45deg, #e74c3c, #f39c12);">🍙</div>
            <div class="gallery-item" style="background: linear-gradient(45deg, #9b59b6, #34495e);">🍥</div>
            <div class="gallery-item" style="background: linear-gradient(45deg, #1abc9c, #f39c12);">🐟</div>
            <div class="gallery-item" style="background: linear-gradient(45deg, #34495e, #e74c3c);">🍱</div>
            <div class="gallery-item" style="background: linear-gradient(45deg, #d35400, #8e44ad);">🥢</div>
        </div>
    </section>

       <section id="contacts">
        <h2 class="section-title">Контакты</h2>
        <div class="history-content">
            <div class="history-text">
                <p>Мы всегда рады видеть вас в нашем ресторане и готовы ответить на все ваши вопросы.</p>
                <p><strong>Адрес:</strong> Tokyo, street 15, restaurant SushiCom</p>
                <p><strong>Часы работы:</strong> ежедневно с 11:00 до 23:00</p>
      </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">✉️</div>
                    <div>
                        <h3>Email</h3>
                        <p>sushiCom15tokio@gmail.com</p>
                    </div>
                    
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Имя</label>
                    <input type="text" id="name" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" required>
                </div>
                
                <div class="form-group">
                    <label for="message">Сообщение</label>
                    <textarea id="message" rows="5" required></textarea>
                </div>
                <button type="submit" class="submit-btn">Отправить</button>
            </form>
  <footer>
        <div class="footer-content">
            <p>© 2025 SushiCom. Все права защищены.</p>
            <div class="social-links">
                <a href="#" class="social-link">📘</a>
                <a href="#" class="social-link">📷</a>
                <a href="#" class="social-link">🐦</a>
            </div>
        </div>

    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
