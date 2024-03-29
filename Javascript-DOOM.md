Claro, aquí tienes un ejemplo detallado de cómo puedes utilizar JavaScript para acceder y modificar el DOM (Document Object Model) de una página web en tiempo real:

Supongamos que tienes una página web con un botón y un párrafo, y quieres cambiar el contenido del párrafo cuando se hace clic en el botón.

1. **HTML**: Primero, creamos la estructura básica en HTML.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manipulación del DOM</title>
</head>
<body>
    <button id="changeTextBtn">Cambiar texto</button>
    <p id="paragraph">Este es un párrafo de ejemplo.</p>

    <script src="script.js"></script> <!-- Vinculamos nuestro archivo JavaScript -->
</body>
</html>
```

2. **JavaScript**: Luego, escribimos el código JavaScript para acceder y modificar el DOM.

```javascript
// Esperamos a que se cargue completamente el contenido HTML
document.addEventListener("DOMContentLoaded", function() {
    // Accedemos al botón y al párrafo por su id
    var button = document.getElementById("changeTextBtn");
    var paragraph = document.getElementById("paragraph");

    // Añadimos un event listener al botón
    button.addEventListener("click", function() {
        // Modificamos el contenido del párrafo
        paragraph.textContent = "¡El texto ha sido cambiado con JavaScript!";
        
        // Cambiamos el estilo del párrafo
        paragraph.style.color = "blue";
        paragraph.style.fontWeight = "bold";
    });
});
```

En este ejemplo:

- Utilizamos `document.getElementById()` para obtener referencias al botón y al párrafo en el DOM.
- Luego, añadimos un event listener al botón que escucha el evento de clic.
- Cuando se hace clic en el botón, modificamos el contenido del párrafo utilizando `textContent`.
- También cambiamos algunos estilos del párrafo utilizando las propiedades de estilo de JavaScript, como `color` y `fontWeight`.

Este es solo un ejemplo básico de manipulación del DOM. Con JavaScript, puedes realizar una amplia variedad de operaciones, como agregar y eliminar elementos, cambiar clases y atributos, animar elementos y mucho más. La manipulación del DOM es fundamental para crear interactividad y dinamismo en las páginas web modernas.

## EJEMPLO 2

Por supuesto, aquí tienes un ejemplo más visual y completo que incluye HTML, CSS y JavaScript para la manipulación del DOM:

**HTML:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manipulación del DOM</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <button id="changeTextBtn">Cambiar texto</button>
    <p id="paragraph">Haz clic en el botón para cambiar este texto.</p>

    <script src="script.js"></script>
</body>
</html>
```

**CSS (styles.css):**

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    padding: 20px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

p {
    font-size: 18px;
    color: #333;
    margin-top: 20px;
}
```

**JavaScript (script.js):**

```javascript
document.addEventListener("DOMContentLoaded", function() {
    var button = document.getElementById("changeTextBtn");
    var paragraph = document.getElementById("paragraph");

    button.addEventListener("click", function() {
        paragraph.textContent = "¡El texto ha sido cambiado con JavaScript!";
        paragraph.style.color = "blue";
        paragraph.style.fontWeight = "bold";
    });
});
```

En este ejemplo, hemos agregado estilos CSS para mejorar la apariencia de la página y hacerla más visualmente atractiva. El JavaScript sigue siendo el mismo, pero ahora la página tiene un aspecto más profesional gracias al CSS. Cuando hagas clic en el botón, el texto del párrafo cambiará y se aplicarán estilos adicionales, como color y peso de la fuente.

Este ejemplo proporciona una visión más completa de cómo puedes manipular el DOM con JavaScript mientras utilizas estilos CSS para mejorar la apariencia de la página.
