# Ex.08 Design of Interactive Image Gallery
## Date:24/12/2025
## ref no: 25017622

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html>
<head>
    <title>bike Gallery</title>
    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            margin: 0;
            padding: 0;
            background: #131212;
            color: rgb(228, 118, 118);
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        .header {
            text-align: center;
            padding: 25px;
            background: linear-gradient(90deg, #b30000, #1a1a1a);
            width: 100%;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.6);
        }

        .header h1 {
            font-size: 2.6rem;
            margin: 0;
            color: #ffffff;
            letter-spacing: 2px;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            padding: 25px;
            width: 90%;
            max-width: 1200px;
        }

        .gallery-item {
            border-radius: 12px;
            overflow: hidden;
            cursor: pointer;
            border: 3px solid #b30000;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            background: #1a1a1a;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 0 25px rgba(255, 0, 0, 0.5);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        .gallery-item:nth-child(1),
        .gallery-item:nth-child(3),
        .gallery-item:nth-child(6) {
            grid-column: span 2;
        }

        .gallery-item::after {
            content: "View bike";
            position: absolute;
            inset: 0;
            background: rgba(0, 0, 0, 0.6);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.3rem;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        #lightbox {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 80%;
            border-radius: 12px;
            box-shadow: 0 0 20px rgba(255, 0, 0, 0.6);
        }

        #lightbox .close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 3rem;
            background: none;
            color: white;
            border: none;
            cursor: pointer;
        }

        .footer {
            width: 100%;
            text-align: center;
            padding: 12px;
            background: #1a1a1a;
            color: #bbbbbb;
            font-size: 1rem;
        }
    </style>
</head>

<body>

<div class="header">
    <h1>BIKE GALLERY</h1>
</div>

<div class="gallery">
    <div class="gallery-item">
        <img src="img1.avif" alt="bike 1">
    </div>
    <div class="gallery-item">
        <img src="img2.avif" alt="bike 2">
    </div>
    <div class="gallery-item">
        <img src="img3.avif" alt="bike 3">
    </div>
    <div class="gallery-item">
        <img src="img4.jpg" alt="bike 4">
    </div>
    <div class="gallery-item">
        <img src="img5.webp" alt="bike 5">
    </div>
    <div class="gallery-item">
        <img src="img6.png" alt="bike 6">
    </div>
    <div class="gallery-item">
        <img src="img7.jpg" alt="bike 7">
    </div>
</div>

<div id="lightbox">
    <button class="close" onclick="closeLightbox()">X</button>
    <img id="lightbox-img">
</div>

<div class="footer">
    <p><b>Designed by AK GOWTHAMAN (25017622)</b></p>
</div>

<script>
    const items = document.querySelectorAll('.gallery-item');

    items.forEach(item => {
        item.addEventListener('click', () => {
            document.getElementById('lightbox-img').src =
                item.querySelector('img').src;
            document.getElementById('lightbox').style.display = 'flex';
        });
    });

    function closeLightbox() {
        document.getElementById('lightbox').style.display = 'none';
    }
</script>

</body>
</html>
~~~

## OUTPUT:
![alt text](<Screenshot 2025-12-27 090957.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
