Aquí tienes un ejemplo de página web sobre tareas diarias del hogar que cumple con las especificaciones de compatibilidad con múltiples dispositivos, utilizando HTML, CSS y JavaScript:

**HTML (index.html):**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tareas del Hogar</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Tareas del Hogar</h1>
    </header>
    
    <main>
        <div id="taskList">
            <h2>Lista de Tareas</h2>
            <ul id="tasks">
                <!-- Aquí se agregarán dinámicamente las tareas -->
            </ul>
            <input type="text" id="taskInput" placeholder="Agregar nueva tarea">
            <button id="addTaskBtn">Agregar</button>
        </div>
    </main>

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
    background-color: #f0f0f0;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
    text-align: center;
}

#taskList {
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    margin: 20px auto;
    max-width: 600px;
}

#tasks {
    list-style-type: none;
    padding: 0;
}

#tasks li {
    margin-bottom: 10px;
}

input[type="text"] {
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 5px;
    width: 70%;
    margin-right: 10px;
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
```

**JavaScript (script.js):**

```javascript
document.addEventListener("DOMContentLoaded", function() {
    var taskInput = document.getElementById("taskInput");
    var addTaskBtn = document.getElementById("addTaskBtn");
    var tasksList = document.getElementById("tasks");

    addTaskBtn.addEventListener("click", function() {
        var taskText = taskInput.value.trim();
        if (taskText !== "") {
            var taskItem = document.createElement("li");
            taskItem.textContent = taskText;
            tasksList.appendChild(taskItem);
            taskInput.value = ""; // Limpiar el input después de agregar la tarea
        }
    });
});
```

Este ejemplo muestra una página web simple sobre tareas del hogar. Los estilos CSS hacen que la página sea atractiva y responsiva, y el JavaScript permite agregar nuevas tareas a la lista dinámicamente sin necesidad de recargar la página. La página es compatible con una amplia variedad de dispositivos y plataformas, ya que JavaScript se ejecuta en el navegador del cliente.
