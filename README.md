<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Presentation Title</title>
    <link rel="stylesheet" href="styles.css">
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-EM2YSJ75N3"></script>
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag() { dataLayer.push(arguments); }
        gtag('js', new Date());
        gtag('config', 'G-EM2YSJ75N3');
    </script>
    <script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_GA_TRACKING_ID"></script>
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'YOUR_GA_TRACKING_ID');
    </script>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            overflow: hidden;
            background-color: #000;
        }

        .container {
            position: relative;
            width: 100vw;
            height: 100vh;
        }

        .slide {
            position: absolute;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f0f0;
            opacity: 0;
            transform: translateX(100%);
            transition: opacity 1s ease, transform 1s ease;
        }

        .slide.active {
            opacity: 1;
            transform: translateX(0);
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="slide active">
            <iframe loading="lazy" src="https://www.canva.com/design/DAGcpgRQm5g/m5X6n6fgsvno_HztzdGBHw/view?embed" allowfullscreen></iframe>
        </div>
        <div class="slide">
            <iframe loading="lazy" src="https://www.canva.com/design/DAGcpgRQm5g/m5X6n6fgsvno_HztzdGBHw/view?embed" allowfullscreen></iframe>
        </div>
    </div>

    <script>
        let slides = document.querySelectorAll(".slide");
        let currentSlide = 0;

        function showNextSlide() {
            slides[currentSlide].classList.remove("active");
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add("active");
        }

        setInterval(showNextSlide, 5000); // Change slide every 5 seconds
    </script>
</body>

</html>
