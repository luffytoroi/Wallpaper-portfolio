<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wallpaper Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            padding: 20px;
        }
        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const gallery = document.querySelector(".gallery");
            for (let i = 1; i <= 8; i++) {  // Adjusted for 01 to 08 naming
                let img = document.createElement("img");
                let num = i.toString().padStart(2, '0'); // Formats 1 as '01', 2 as '02', etc.
                img.src = `wallpapers/${num}.jpg`; // Assumes images are named 01.jpg, 02.jpg, etc.
                img.alt = `Wallpaper ${num}`;
                gallery.appendChild(img);
            }
        });
    </script>
</head>
<body>
    <h1>Wallpaper Gallery</h1>
    <div class="gallery"></div>
</body>
</html>
