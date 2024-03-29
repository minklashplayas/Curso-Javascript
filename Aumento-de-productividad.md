Claro, aquí tienes un ejemplo de una página web para completar tareas que primero se agregan y luego se pueden marcar como completadas, aprovechando el aumento de la productividad que ofrece JavaScript:

**HTML (index.html):**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Tareas</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Lista de Tareas</h1>
    </header>
    
    <main>
        <div id="taskList">
            <h2>Tareas Pendientes</h2>
            <ul id="pendingTasks">
                <!-- Aquí se agregarán dinámicamente las tareas pendientes -->
            </ul>
            <input type="text" id="taskInput" placeholder="Agregar nueva tarea">
            <button id="addTaskBtn">Agregar</button>
        </div>

        <div id="completedList" style="display: none;">
            <h2>Tareas Completadas</h2>
            <ul id="completedTasks">
                <!-- Aquí se agregarán dinámicamente las tareas completadas -->
            </ul>
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
    margin-bottom: 20px;
}

#completedList {
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    display: none;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
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

.completed {
    text-decoration: line-through;
    color: #aaa;
}
```

**JavaScript (script.js):**

```javascript
document.addEventListener("DOMContentLoaded", function() {
    var taskInput = document.getElementById("taskInput");
    var addTaskBtn = document.getElementById("addTaskBtn");
    var pendingTasksList = document.getElementById("pendingTasks");
    var completedTasksList = document.getElementById("completedTasks");

    addTaskBtn.addEventListener("click", function() {
        var taskText = taskInput.value.trim();
        if (taskText !== "") {
            var taskItem = document.createElement("li");
            taskItem.textContent = taskText;

            var completeButton = document.createElement("button");
            completeButton.textContent = "Completar";
            completeButton.className = "completeBtn";

            taskItem.appendChild(completeButton);
            pendingTasksList.appendChild(taskItem);
            taskInput.value = ""; // Limpiar el input después de agregar la tarea

            completeButton.addEventListener("click", function() {
                var parentItem = this.parentElement;
                parentItem.removeChild(this);
                parentItem.classList.add("completed");
                completedTasksList.appendChild(parentItem);
            });
        }
    });
});
```

En este ejemplo:

- Se puede agregar una tarea escribiendo su descripción en el campo de texto y haciendo clic en el botón "Agregar".
- Las tareas se agregan como elementos de lista (`<li>`) en la lista de tareas pendientes (`pendingTasksList`).
- Cada tarea pendiente tiene un botón "Completar" que permite marcar la tarea como completada.
- Cuando se hace clic en el botón "Completar", la tarea se mueve a la lista de tareas completadas (`completedTasksList`) y se tacha su descripción.
- La página utiliza CSS para darle estilo y hacerla más atractiva, y JavaScript para agregar funcionalidad dinámica y aumentar la productividad al permitir la gestión eficiente de las tareas.
