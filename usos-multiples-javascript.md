Claro, aquí tienes un ejemplo de una página web HTML con CSS y JavaScript integrados en múltiples aspectos de uso:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Web con HTML, CSS y JavaScript</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>¡Bienvenido!</h1>
    </header>
    
    <main>
        <div id="content">
            <h2>Contenido Dinámico</h2>
            <p id="dynamicText">Este texto cambiará con JavaScript.</p>
            <button id="changeTextBtn">Cambiar Texto</button>
        </div>

        <div id="imageGallery">
            <h2>Galería de Imágenes</h2>
            <div class="imageContainer">
                <img src="image1.jpg" alt="Imagen 1">
                <p>Descripción de la imagen 1.</p>
            </div>
            <div class="imageContainer">
                <img src="image2.jpg" alt="Imagen 2">
                <p>Descripción de la imagen 2.</p>
            </div>
        </div>
    </main>

    <footer>
        <p>© 2024 - Página Web creada por ChatGPT</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```

**CSS (styles.css):**

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

#content {
    margin-bottom: 20px;
}

h2 {
    color: #4CAF50;
}

#imageGallery {
    display: flex;
    justify-content: space-around;
}

.imageContainer {
    text-align: center;
    margin-bottom: 20px;
}

img {
    width: 100%;
    max-width: 300px;
    border-radius: 5px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
}
```

**JavaScript (script.js):**

```javascript
document.addEventListener("DOMContentLoaded", function() {
    var dynamicText = document.getElementById("dynamicText");
    var changeTextBtn = document.getElementById("changeTextBtn");
    var imageContainers = document.querySelectorAll(".imageContainer");

    changeTextBtn.addEventListener("click", function() {
        dynamicText.textContent = "¡El texto ha sido cambiado con JavaScript!";
    });

    imageContainers.forEach(function(container) {
        container.addEventListener("mouseenter", function() {
            var img = container.querySelector("img");
            img.style.opacity = "0.7";
        });

        container.addEventListener("mouseleave", function() {
            var img = container.querySelector("img");
            img.style.opacity = "1";
        });
    });
});
```

En este ejemplo:

- La página web tiene un encabezado (`header`), un contenido principal (`main`) y un pie de página (`footer`).
- El contenido principal contiene dos secciones: una con contenido dinámico que cambia con JavaScript (`#content`), y otra con una galería de imágenes (`#imageGallery`).
- Se utiliza CSS para dar estilo a la página y hacerla más atractiva.
- JavaScript agrega interactividad al cambiar dinámicamente el texto en respuesta al clic en un botón (`#changeTextBtn`), y al cambiar la opacidad de las imágenes en la galería cuando se pasa el cursor sobre ellas.
