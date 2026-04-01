# Ex.07 Design of Interactive Image Gallery
## Date:17-03-2026

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
gallery.html
<html>
  <head>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <section>
      <h1>Image Gallery</h1>
      <div class="slider">
       <img id="display" src="a1.jpg" />

    <div class="controls">
        <button onclick="change(-1)">Previous</button>
        <button onclick="change(1)">Next</button>
    </div>
    </section>

    <script>
      const images = ["a1.jpg", "a2.jpg", "a3.jpg", "a4.jpg", "a5.jpg"];
      let index = 0;

      function change(step) {
        index = (index + step + images.length) % images.length;
        document.getElementById("display").src = images[index];
      }
      
    </script>
    <footer>
      <p>Desinged by Manorajapriyan.l.e</p>
    </footer>
  </body>
    
</html>

style.css
body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgb(242, 255, 240);
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

section {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  font-size: 24px;
  margin-bottom: 15px;
}

.slider {
  width: 800px;
  max-width: 90%;
  background: black;
  border-radius: 15px;
  padding: 10px;
  text-align: center;
  box-shadow: 0 20px 40px rgba(72, 141, 211, 0.904);
}

.slider img {
  width: 100%;
  height: 450px;
  object-fit: contain;
  border-radius: 15px;
}

.controls {
  margin-top: 12px;
  display: flex;
  justify-content: space-between;
}

.controls button {
  flex: 1;
  margin: 5px;
  padding: 10px;
  font-size: 16px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  background: #333;
  color: white;
  transition: 0.3s;
}

.controls button:hover {
  background: #555;
}

.controls button:active {
  transform: scale(0.95);
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  text-align: center;
  background: #fcfbfb;
  color: rgb(10, 0, 0);
  padding: 10px;
  font-size: 20px;
}
```

## OUTPUT:
![alt text](<Screenshot (38).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
