<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sylwestrowa Galeria Zdjęć</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-image: url('https://www.folgagryfice.pl/pliki/sylwester.webp'); /* Wstaw link do tła */
            background-size: cover;
            background-position: center;
            color: white;
        }
        #upload-container {
            margin-top: 50px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
            display: inline-block;
        }
        #gallery {
            margin-top: 20px;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
        }
        .photo {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border: 2px solid white;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>Witaj w Sylwestrowej Galerii Zdjęć!</h1>
    <div id="upload-container">
        <input type="file" id="fileInput" accept="image/*">
        <button onclick="uploadPhoto()">Dodaj zdjęcie</button>
    </div>
    <div id="gallery"></div>

    <script>
        const gallery = document.getElementById('gallery');

        function uploadPhoto() {
            const fileInput = document.getElementById('fileInput');
            const file = fileInput.files[0];

            if (file) {
                const reader = new FileReader();
                reader.onload = function(event) {
                    const img = document.createElement('img');
                    img.src = event.target.result;
                    img.className = 'photo';
                    gallery.appendChild(img);
                };
                reader.readAsDataURL(file);
            } else {
                alert('Wybierz plik przed dodaniem!');
            }
        }
    </script>
</body>
</html>
