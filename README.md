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
      background-color: #f4f4f4;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
      width: 80%;
      max-width: 900px;
    }

    .gallery img {
      width: 100%;
      height: auto;
      border-radius: 10px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .gallery img:hover {
      transform: scale(1.1);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    }

    /* Modal Styles */
    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      display: none;
      justify-content: center;
      align-items: center;
    }

    .modal img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
    }

    .modal-close {
      position: absolute;
      top: 20px;
      right: 20px;
      background-color: #fff;
      border: none;
      font-size: 18px;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 5px;
    }

    .modal-close:hover {
      background-color: #ccc;
    }
  </style>
</head>
<body>

  <div class="gallery">
    <img src="https://via.placeholder.com/300/FF5733" alt="Image 1">
    <img src="https://via.placeholder.com/300/33FF57" alt="Image 2">
    <img src="https://via.placeholder.com/300/3357FF" alt="Image 3">
    <img src="https://via.placeholder.com/300/F3FF33" alt="Image 4">
    <img src="https://via.placeholder.com/300/FF33F3" alt="Image 5">
    <img src="https://via.placeholder.com/300/33FFF3" alt="Image 6">
  </div>

  <!-- Modal -->
  <div class="modal" id="modal">
    <button class="modal-close" onclick="closeModal()">Close</button>
    <img id="modal-img" src="" alt="Modal Image">
  </div>

  <script>
    const gallery = document.querySelectorAll('.gallery img');
    const modal = document.getElementById('modal');
    const modalImg = document.getElementById('modal-img');

    gallery.forEach(img => {
      img.addEventListener('click', () => {
        modal.style.display = 'flex';
        modalImg.src = img.src;
      });
    });

    function closeModal() {
      modal.style.display = 'none';
    }

    // Close modal when clicking outside the image
    modal.addEventListener('click', (e) => {
      if (e.target === modal) {
        closeModal();
      }
    });
  </script>

</body>
</html>
