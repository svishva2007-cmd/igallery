# Ex.08 Design of Interactive Image Gallery
## Date:24.12.2025
## Register number:25006451

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
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Animated Image Gallery</title>

  <style>
    body {
      font-family: "Segoe UI", Arial, sans-serif;
      background: linear-gradient(135deg, #667eea, #764ba2);
      margin: 0;
      padding: 30px;
      text-align: center;
      min-height: 100vh;
    }

    h1 {
      color: #ffffff;
      margin-bottom: 25px;
      letter-spacing: 2px;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      justify-content: center;
    }

    .gallery img {
      width: 160px;
      height: 110px;
      object-fit: cover;
      cursor: pointer;
      border-radius: 12px;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
    }

    .gallery img:hover {
      transform: scale(1.1);
      box-shadow: 0 12px 30px rgba(0,0,0,0.5);
    }

    .modal {
      display: flex;
      position: fixed;
      inset: 0;
      background: rgba(3, 241, 98, 0.85);
      justify-content: center;
      align-items: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.4s ease;
      z-index: 1000;
    }

    .modal.active {
      opacity: 1;
      pointer-events: auto;
    }

    .modal img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 15px;
      transform: scale(0.7);
      transition: transform 0.4s ease;
    }

    .modal.active img {
      transform: scale(1);
    }

    .modal-close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 35px;
      color: rgba(12, 209, 206, 0.755);
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .modal-close:hover {
      transform: rotate(90deg) scale(1.2);
    }
  </style>
</head>

<body>

  <h1>Animated Image Gallery</h1>

  <div class="gallery">
    <img src="chess.jpg" alt="Image 1">
    <img src="my photo.jpeg" alt="Image 2">
    <img src="thousand window house.webp" alt="Image 3">
    <img src="aranmanai.webp" alt="Image 4">
    <img src="spider-man_5120x2880_xtrafondos.com.jpg" alt="Image 5">
  </div>

  <div class="modal" id="imageModal">
    <span class="modal-close" id="closeModal">&times;</span>
    <img id="modalImg" src="" alt="Large View">
  </div>

  <script>
    const galleryImages = document.querySelectorAll(".gallery img");
    const modal = document.getElementById("imageModal");
    const modalImg = document.getElementById("modalImg");
    const closeModal = document.getElementById("closeModal");

    galleryImages.forEach(img => {
      img.addEventListener("click", () => {
        modalImg.src = img.src;
        modal.classList.add("active");
      });
    });

    closeModal.addEventListener("click", () => {
      modal.classList.remove("active");
    });

    modal.addEventListener("click", e => {
      if (e.target === modal) {
        modal.classList.remove("active");
      }
    });
  </script>

</body>
</html>
~~~

## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c202a6f2-8a25-4a01-9a75-17051b721e03" />


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
