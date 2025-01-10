# Image_gallery
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
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
      transition: transform 0.3s;
    }
    .gallery img:hover {
      transform: scale(1.1);
    }
  </style>
</head>
<body>
  <h1 style="text-align: center;">Image Gallery</h1>
  <div class="gallery">
    <img src="https://via.placeholder.com/150" alt="Image 1">
    <img src="https://via.placeholder.com/150" alt="Image 2">
    <img src="https://via.placeholder.com/150" alt="Image 3">
    <img src="https://via.placeholder.com/150" alt="Image 4">
    <img src="https://via.placeholder.com/150" alt="Image 5">
  </div>
</body>
</html>
