# Ex.08 Design of Interactive Image Gallery
## Date:

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
```
<h2 align="center">TOP SIX SCI-FI MOVIES</h2>
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
  background-color: #f0f0f0;
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
  width: 500px;
  height: 400px;
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
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  overflow: auto;
}

.modal-content {
  display: block;
  margin: auto;
  max-width: 80%;
  max-height: 80%;
}

.close {
  color: #fff;
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
<body>

  <div class="gallery">
    <div class="image-container">
      <img src="C:\Users\admin\Pictures\Saved Pictures\INCEPTION.jpg"  alt="INCEPTION" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="C:\Users\admin\Pictures\Saved Pictures\images (3).jpg"  alt="INTERSTELLAR" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="C:\Users\admin\Pictures\Saved Pictures\images (4).jpg"  alt="ALIEN" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="C:\Users\admin\Pictures\Saved Pictures\images (5).jpg" alt="2001" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="C:\Users\admin\Pictures\Saved Pictures\images (6).jpg"  alt="TERMINATOR" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="C:\Users\admin\Pictures\Saved Pictures\images (7).jpg"  alt="OPPENHEIMER" class="gallery-item">
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
    <h2 align="center">Designed and developed by VISHNU RATHAN</h2>
  </footer>
</body>
</html>
```

## OUTPUT:

![Screenshot 2024-12-26 144004](https://github.com/user-attachments/assets/145c1553-b4d6-4abf-aa01-06d1a27b8118)
![Screenshot 2024-12-26 144020](https://github.com/user-attachments/assets/0559d418-3f6b-4ce7-89d4-3d98e04a9347)
![Screenshot 2024-12-26 144036](https://github.com/user-attachments/assets/095debe9-4d52-4e83-9e79-938507592a65)
![Screenshot 2024-12-26 144045](https://github.com/user-attachments/assets/f78f8e9f-8413-49e6-8e89-e70427a48358)



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
