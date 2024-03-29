Por supuesto, aquí tienes un ejemplo más extenso y funcional de una página web que utiliza HTML, CSS y JavaScript de manera integral:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Página Web</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>¡Bienvenido a mi Página Web!</h1>
    </header>
    
    <nav>
        <ul>
            <li><a href="#section1">Sección 1</a></li>
            <li><a href="#section2">Sección 2</a></li>
            <li><a href="#section3">Sección 3</a></li>
        </ul>
    </nav>
    
    <main>
        <section id="section1">
            <h2>Sección 1</h2>
            <p>Este es un ejemplo de una sección de contenido en mi página web.</p>
        </section>
        
        <section id="section2">
            <h2>Sección 2</h2>
            <p>Esta es otra sección con contenido interesante.</p>
        </section>
        
        <section id="section3">
            <h2>Sección 3</h2>
            <p>¡Aquí encontrarás aún más contenido emocionante!</p>
        </section>
    </main>

    <footer>
        <p>© 2024 - Mi Página Web</p>
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

nav ul {
    list-style-type: none;
    padding: 0;
    text-align: center;
}

nav ul li {
    display: inline;
    margin-right: 20px;
}

nav ul li a {
    text-decoration: none;
    color: #333;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 40px;
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
    var navLinks = document.querySelectorAll("nav ul li a");

    navLinks.forEach(function(link) {
        link.addEventListener("click", function(event) {
            event.preventDefault();
            var targetId = this.getAttribute("href").substring(1);
            var targetSection = document.getElementById(targetId);
            targetSection.scrollIntoView({ behavior: "smooth" });
        });
    });
});
```

En este ejemplo:

- La página web tiene un encabezado (`header`), un menú de navegación (`nav`), un contenido principal (`main`) y un pie de página (`footer`).
- El menú de navegación contiene enlaces que llevan a diferentes secciones de la página.
- CSS se utiliza para dar estilo a la página y hacerla más atractiva y legible.
- JavaScript se utiliza para añadir un efecto de desplazamiento suave cuando se hace clic en los enlaces del menú de navegación, lo que mejora la experiencia del usuario al navegar por la página.
