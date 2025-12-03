<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Table Tennis</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

    <style>
        /* Общие стили */
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: "Segoe UI", Arial, sans-serif;
            background: linear-gradient(to bottom right, #0a1228, #1b263b);
            color: white;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .hero-header {
            background: linear-gradient(90deg, #061d43, #000000);
            padding: 60px 20px;
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.5);
        }

        .hero-header h1 {
            font-size: 55px;
            font-family: wide latin;
            text-shadow: 0 0 15px rgb(12,0,83);
        }

        .hero-header p {
            font-size: 18px;
            opacity: 0.8;
        }

        nav {
            position: sticky;
            top: 0;
            background: rgba(15, 25, 45, 0.9);
            backdrop-filter: blur(6px);
            box-shadow: 0 2px 8px rgba(0,0,0,0.4);
            z-index: 50;
            font-family: wide latin;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 12px;
            flex-wrap: wrap;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 5px 15px;
            padding: 8px 18px;
            border-radius: 25px;
            transition: 0.3s;
        }

        nav a:hover,
        nav a.active {
            background: rgba(255,255,255,0.2);
            color: #000000;
            box-shadow: 0 0 10px rgba(255,255,255,0.5);
        }

        .carousel-item img {
            height: 480px;
            object-fit: cover;
            border-radius: 20px;
            box-shadow: 0 5px 25px #0a1228;
        }

        .carousel-caption {
            background: rgba(0,0,0,0.65);
            border-radius: 10px;
            padding: 10px 15px;
            font-family: wide latin;
        }

        .main-container {
            display: flex;
            gap: 25px;
            max-width: 1200px;
            margin: 50px auto;
            padding: 0 20px;
        }

        aside {
            width: 25%;
            background: rgba(8,20,40,0.8);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.4);
        }

        aside h2 {
            text-align: center;
            font-family: wide latin;
            margin-bottom: 15px;
        }

        aside a {
            display: block;
            padding: 10px 0;
            text-decoration: none;
            color: #fff;
            transition: 0.3s;
        }

        aside a:hover {
            text-shadow: 0 0 8px rgba(255,255,255,0.7);
        }

        .aside-profile {
            text-align: center;
            margin-top: 20px;
        }

        .aside-profile img {
            width: 100%;
            height: 160px;
            object-fit: cover;
            border-radius: 10px;
            border: 3px solid white;
            box-shadow: 0 4px 12px rgba(255,255,255,0.2);
        }

        .aside-profile p {
            margin-top: 10px;
            font-size: 14px;
            color: #eaeaea;
            line-height: 1.4;
        }

        main {
            flex: 1;
            background: rgba(10,20,45,0.8);
            padding: 35px;
            border-radius: 15px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.4);
        }

        .card {
            background: rgba(10,20,45,0.9);
            padding: 25px;
            color: white;
            border-radius: 15px;
            margin-bottom: 25px;
            border-left: 4px solid white;
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255,255,255,0.2);
        }

        .section-img {
            width: 100%;
            max-width: 500px;
            height: auto;
            display: block;
            margin: 15px auto;
            border: 5px solid #ffffff;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(255,255,255,0.2);
            object-fit: cover;
            background: rgba(255,255,255,0.05);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .gallery-item {
            width: 100%;
            height: 150px;
            border-radius: 12px;
            overflow: hidden;
            border: 4px solid #ffffff;
            box-shadow: 0 4px 15px rgba(255,255,255,0.2);
            background: rgba(255,255,255,0.05);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        footer {
            text-align: center;
            padding: 20px;
            background: rgba(0,0,0,0.85);
            margin-top: 40px;
            box-shadow: 0 -3px 8px rgba(0,0,0,0.4);
            font-size: 14px;
        }

        @media(max-width: 768px){
            .main-container {
                flex-direction: column;
            }

            aside {
                width: 100%;
            }

            .carousel-item img {
                height: 300px;
            }
        }
    </style>
</head>
<body>

<header class="hero-header">
    <h1> Table Tennis</h1>
    <p>Fast. Dynamic. Legendary.</p>
</header>

<nav>
    <ul>
        <li><a href="main.html" class="active">Home</a></li>
        <li><a href="history.html">History</a></li>
        <li><a href="music&video.html">Music & Video</a></li>
        <li><a href="filter.html">Buy Tennis Stuff</a></li>
    </ul>
</nav>

<div class="container mt-4">
    <div id="myCarousel" class="carousel slide" data-bs-ride="carousel">

        <div class="carousel-indicators">
            <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="0" class="active"></button>
            <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="1"></button>
            <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="2"></button>
        </div>

        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="https://media.baamboozle.com/uploads/images/368927/1627466174_840396.jpeg" 
                     class="d-block w-100" alt="Slide 1">
                <div class="carousel-caption d-none d-md-block">
                    <h5>World Table Tennis Championships</h5>
                    <p>2023</p>
                </div>
            </div>

            <div class="carousel-item">
                <img src="https://i.ytimg.com/vi/Lpgi1Perm50/maxresdefault.jpg" 
                     class="d-block w-100" alt="Slide 2">
                <div class="carousel-caption d-none d-md-block">
                    <h5>The deep meaning of Table Tennis</h5>
                    <p>2008</p>
                </div>
            </div>

            <div class="carousel-item">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Flickr_-_Government_Press_Office_%28GPO%29_-_A_Table_Tennis_Competition.jpg/1200px-Flickr_-_Government_Press_Office_%28GPO%29_-_A_Table_Tennis_Competition.jpg" 
                     class="d-block w-100" alt="Slide 3">
                <div class="carousel-caption d-none d-md-block">
                    <h5>Old Table Tennis training rooms</h5>
                    <p>1996</p>
                </div>
            </div>
        </div>

        <button class="carousel-control-prev" type="button" data-bs-target="#myCarousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon"></span>
        </button>

        <button class="carousel-control-next" type="button" data-bs-target="#myCarousel" data-bs-slide="next">
            <span class="carousel-control-next-icon"></span>
        </button>

    </div>
</div>

<div class="container main-container">
   <aside>
    <h2>Menu</h2>
    <ul>
        <li><a href="form.html">Form</a></li>
        <li><a href="register.html">Registration</a></li>
    </ul>

    <div class="aside-profile">
        <img src="https://www.mplgames.com/blog/wp-content/uploads/2025/05/shutterstock_2472326771-2048x1122.jpg">
        <p>Register now and start winning tournaments! Join the game, improve your skills, and compete with the best. Your table tennis journey begins today!</p>
    </div>
   </aside>

   <main>
       <section class="card">
           <h2>What is Table Tennis?</h2>
           <img src="https://cdn.sportmaster.ru/upload/content/mediahab/prod/a388010a-3ca9-4738-9ff4-0db1176ecf69.jpg" 
                alt="Table Tennis Image"
                class="section-img">
           <p>
               Table Tennis is a fast and dynamic sport where two or four players hit a lightweight ball back and forth across a table using small paddles...
           </p>
       </section>

       <section class="card">
           <h2>Skills & Training</h2>
           <img src="https://essentuki.amaks-kurort.ru/upload/iblock/cf8/dlx0ekvhr45no32y249yhkjehynh95cx/a47d6b16_b1d8_5e28_b54d_ede5e423d2e6.png"
                alt="Skills & Training Image"
                class="section-img">
           <ul>
               <li><b>Skills:</b> Quick reflexes, hand–eye coordination, spin control...</li>
               <li><b>Training:</b> Practicing strokes, serves, footwork...</li>
               <li><b>Focus:</b> Mental alertness and concentration...</li>
           </ul>
       </section>

       <section class="card">
           <h2>Gallery</h2>
           <div class="gallery-grid">
               <div class="gallery-item">
                   <img src="file:///C:/Users/nurzh/Downloads/yodarb%20tennis.jpg" alt="Local Image">
               </div>
               <div class="gallery-item">
                   <img src="https://beam-images.warnermediacdn.com/taiga/Specifique/Crop/16_9/20033_0_200077699_20240801-111553.jpeg?host=i.eurosport.com&partner=beamcom&w=500" alt="Gallery Image 2">
               </div>
               <div class="gallery-item">
                   <img src="https://i2.wp.com/www.asoif.com/sites/default/files/styles/default_880/public/news/table_tennis_w03.jpg?itok=134czA-P" alt="Gallery Image 3">
               </div>
               <div class="gallery-item">
                   <img src="https://upload.wikimedia.org/wikipedia/commons/0/09/Table_tennis_at_the_2018_Summer_Youth_Olympics_%E2%80%93_Mixed_Final_Doubles_103.jpg" alt="Gallery Image 4">
               </div>
           </div>
       </section>

       <section class="card">
           <h2>Interesting Facts</h2>
           <p>Table tennis is one of the fastest sports in the world; the ball can reach speeds of over 100 km/h in professional matches...</p>
       </section>
   </main>
</div>

<footer>
    <p>© 2025 Nurzhan | Table Tennis</p>
</footer>

</body>
</html>


