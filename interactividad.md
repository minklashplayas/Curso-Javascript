## INTERACTIVIDAD Javascript - HTML

Por supuesto, aquí tienes un ejemplo detallado de cómo JavaScript puede permitir la interactividad con elementos de una página web, centrándonos en formularios, botones y menús desplegables:

Supongamos que tienes un formulario de contacto en tu página web con campos para nombre, correo electrónico y mensaje. Además, tienes un botón de envío y un menú desplegable para seleccionar el motivo del contacto.

1. **HTML**: Primero, creamos la estructura del formulario en HTML.

```html
<form id="contactForm">
    <label for="name">Nombre:</label>
    <input type="text" id="name" name="name"><br>

    <label for="email">Correo electrónico:</label>
    <input type="email" id="email" name="email"><br>

    <label for="message">Mensaje:</label>
    <textarea id="message" name="message"></textarea><br>

    <label for="reason">Motivo de contacto:</label>
    <select id="reason" name="reason">
        <option value="consulta">Consulta</option>
        <option value="soporte">Soporte técnico</option>
        <option value="comentario">Comentario</option>
    </select><br>

    <button type="submit" id="submitBtn">Enviar</button>
</form>
```

2. **JavaScript**: Luego, utilizamos JavaScript para agregar interactividad al formulario. Por ejemplo, podríamos validar que los campos no estén vacíos antes de enviar el formulario y mostrar un mensaje de error si es necesario.

```javascript
document.getElementById("contactForm").addEventListener("submit", function(event) {
    event.preventDefault(); // Evita que se envíe el formulario automáticamente
    
    // Obtener valores de los campos
    var name = document.getElementById("name").value;
    var email = document.getElementById("email").value;
    var message = document.getElementById("message").value;
    var reason = document.getElementById("reason").value;

    // Validar que los campos no estén vacíos
    if (name.trim() === '' || email.trim() === '' || message.trim() === '') {
        alert("Por favor, complete todos los campos.");
        return;
    }

    // Envío del formulario (simulado)
    // Aquí podrías enviar los datos del formulario a un servidor utilizando AJAX o fetch
    console.log("Nombre: " + name);
    console.log("Correo electrónico: " + email);
    console.log("Mensaje: " + message);
    console.log("Motivo de contacto: " + reason);

    // Reiniciar el formulario después del envío
    document.getElementById("contactForm").reset();
});
```

Con este código, cuando el usuario envíe el formulario, JavaScript interceptará el evento de envío, validará los campos y, si están completos, imprimirá los valores en la consola del navegador (puedes reemplazar esto con una solicitud AJAX real). Luego, reiniciará el formulario para futuros usos.

Este ejemplo muestra cómo JavaScript permite la interactividad en un formulario web al validar campos y manejar eventos de envío. Similarmente, puedes agregar interactividad a botones y menús desplegables para crear una experiencia de usuario más dinámica y atractiva en tu página web.

## SU CSS Respinsive

¡Por supuesto! A continuación, te proporciono un ejemplo de CSS utilizando flexbox para crear un diseño responsive que se adapte a dispositivos móviles y de escritorio:

```css
/* Estilos generales */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 800px; /* Ancho máximo del contenido */
    margin: 0 auto; /* Centrar el contenido */
    padding: 20px;
    box-sizing: border-box; /* Incluir padding en el ancho total */
}

/* Estilos del formulario */
form {
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
}

input[type="text"],
input[type="email"],
textarea,
select,
button {
    margin-bottom: 10px;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
    width: 100%; /* Ocupar todo el ancho disponible */
}

button {
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

/* Estilos para dispositivos móviles */
@media only screen and (max-width: 600px) {
    .container {
        padding: 10px;
    }
}

/* Estilos para pantallas más grandes (PC) */
@media only screen and (min-width: 601px) {
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }

    form {
        width: 50%;
    }
}
```

Con estos estilos CSS, el formulario se adaptará de la siguiente manera:

- En dispositivos móviles con un ancho de pantalla máximo de 600px, el contenido se ajustará para ser más compacto y fácil de leer.
- En pantallas más grandes (PC) con un ancho de pantalla mínimo de 601px, el formulario estará centrado en la pantalla y ocupará el 50% del ancho disponible.

Este enfoque utiliza media queries para aplicar diferentes estilos dependiendo del tamaño de la pantalla del dispositivo, lo que garantiza una experiencia de usuario óptima tanto en dispositivos móviles como de escritorio.
