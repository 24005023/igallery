# Ex.07 Design of Interactive Image Gallery
## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```
<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 
  <title>Image Gallery</title>
  

  <link rel="stylesheet" href="styles.css">

</head>
<style>
 
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #00000000;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 20px;
}

.image-container {
  position: relative;
  overflow: hidden;
  
  height: 550px;
}

.gallery-item {
  width: 100%;
  height: auto;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.1);
}


.modal {
  display: none; 
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 80%;
  height: 80%;
  background-color: rgba(0, 0, 0, 0.9);
  overflow: auto;
}

.modal-content {
  display: block;
  margin: auto;
  max-width: 70%;
  max-height: 70%;
}

.close {
  color: #ffffff00;
  font-size: 40px;
  font-weight: bold;
  position: absolute;
  top: 10px;
  right: 25px;
  transition: 0.3s;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #ddd;
  text-decoration: none;
  cursor: pointer;
}

#caption {
  text-align: center;
  color: #fff;
  font-size: 20px;
  padding: 10px;
}

</style>
<body align="center">
<h1>INTERACTIVE IMAGE GALLERY</h1>
  <div class="gallery">
    <div class="image-container">
      <img src="c:\Users\admin\igallery\raj\calcapp\static\vijay.avif"  alt="BEACH" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="c:\Users\admin\igallery\raj\calcapp\static\ajith.webp"  alt="FLOWER" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="c:\Users\admin\igallery\raj\calcapp\static\surya.jpg"  alt="MOUNTAIN" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="c:\Users\admin\igallery\raj\calcapp\static\jackie-chan.avif" alt="Rain" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="c:\Users\admin\igallery\raj\calcapp\static\ar rahuman.jpeg"  alt="ROAD" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="c:\Users\admin\igallery\raj\calcapp\static\billgates.jpg"  alt="WHITE FLOWER" class="gallery-item">
    </div>
    
  </div>

  
  <div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="img01">
    <div id="caption"></div>
  </div>

  <script>
  
const modal = document.getElementById("myModal");
const modalImg = document.getElementById("img01");
const captionText = document.getElementById("caption");
const closeBtn = document.getElementsByClassName("close")[0];


const images = document.querySelectorAll(".gallery-item");


images.forEach(img => {
  img.onclick = function() {
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
  };
});


closeBtn.onclick = function() {
  modal.style.display = "none";
};


window.onclick = function(event) {
  if (event.target === modal) {
    modal.style.display = "none";
  }
};

  </script>
  <footer>
    <h3>Designed and developed by Rajkumar T</h3>
  </footer>
</body>
</html>
```
## OUTPUT:
<img width="1067" height="419" alt="Screenshot 2026-05-26 104546" src="https://github.com/user-attachments/assets/1a31b4d9-cef6-4bde-87bc-7706409de9e4" />

<img width="1045" height="415" alt="Screenshot 2026-05-26 104603" src="https://github.com/user-attachments/assets/68aa5973-62b3-4e40-b51c-d9e15bb0f095" />


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
