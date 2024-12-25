# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Photo Gallery</title>
  <link rel="stylesheet" href="gallery.css">
</head>
<body>
  <header>
    <h1>INTERACTIVE IMAGE GALLERY</h1>
  </header>
  <main>
    <section class="gallery">
      <div class="photo-item" data-title="BRENDON MCCULLUM">
        <img src="image1.jpg" alt="BRENDON MCCULLUM">
      </div>
      <div class="photo-item" data-title="AB DEVILLERS">
        <img src="image2.jpg" alt="AB DEVILLERS">
      </div>
      <div class="photo-item" data-title="KUMAR SANGAKKARA">
        <img src="image3.jpg" alt="KUMAR SANGAKKARA">
      </div>
      <div class="photo-item" data-title="VIRAT KHOLI">
        <img src="image4.jpg" alt="VIRAT KHOLI">
      </div>
      <div class="photo-item" data-title="DAVID WARNER">
        <img src="image5.jpg" alt="DAVID WARNER">
      </div>
      <div class="photo-item" data-title="EOIN MORGAN">
        <img src="image6.jpg" alt="EOIN MORGAN">
      </div>
      <div class="photo-item" data-title="CHRIS GAYLE">
        <img src="image7.jpg" alt="CHRIS GAYLE">
      </div>
      <div class="photo-item" data-title="KANE WILLIAMSON">
        <img src="image8.jpg" alt="KANE WILLIAMSON">
      </div>
    </section>
  </main>

  <div id="lightbox" class="lightbox" onclick="closeLightbox()">
    <img id="lightbox-img" src="" alt="Large View">
  </div>
 <script src="gallery.js"></script>
</body>
</html>



body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: darkseagreen;
  }
  
  header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem;
  }
  
  header h1 {
    margin: 0;
  }
  main {
    padding: 5rem;
  }
  
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 10rem;

  }
  
  .photo-item img {
    width: 100%;
    height: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    transition: transform 0.3s ease;
  }
  
  .photo-item img:hover {
    transform: scale(1.05);
  }
  
  .lightbox {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
  }
  
  .lightbox img {
    max-width: 90%;
    max-height: 90%;
  }


  const photoItems = document.querySelectorAll('.photo-item img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');

photoItems.forEach(img => {
  img.addEventListener('click', () => {
    lightbox.style.display = 'flex';
    lightboxImg.src = img.src;
  });
});

function closeLightbox() {
  lightbox.style.display = 'none';
}

function filterImages() {
  const query = document.getElementById('search').value.toLowerCase();
  const photoItems = document.querySelectorAll('.photo-item');
  
  photoItems.forEach(item => {
    const title = item.getAttribute('data-title').toLowerCase();
    if (title.includes(query)) {
      item.style.display = 'block';
    } else {
      item.style.display = 'none';
    }
  });
}
```


# OUTPUT:
![alt text](<Screenshot 2024-12-25 183414.png>)
![alt text](<Screenshot 2024-12-25 183432.png>)


# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
