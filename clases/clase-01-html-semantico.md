# Clase 01: Estructura Básica y HTML Semántico

## 1. Objetivo de la clase
Comprender la anatomía obligatoria de un documento HTML5 y asimilar el concepto de "semántica web" para construir la estructura inicial de nuestra landing page de Uber Tracker de forma accesible y optimizada para buscadores (SEO).

## 2. Explicación en lenguaje claro
Pensá en una página web como en el plano de un edificio o el esqueleto de un cuerpo humano. HTML no define si la página es linda o fea (eso lo hace CSS), sino qué es cada cosa. 
Si tirás texto suelto, el navegador lo va a mostrar, pero de manera "ciega". Al usar etiquetas semánticas, le estamos diciendo al navegador (y a Google): "Esto es el encabezado principal", "Esto es un grupo de enlaces de navegación", "Esto es el pie de página". 

## 3. Concepto técnico mínimo
Todo documento HTML5 moderno requiere un "esqueleto" obligatorio e inalterable:

* `<!DOCTYPE html>`: Le avisa al navegador que use el estándar moderno de HTML5.
* `<html lang="es">`: El contenedor raíz de todo. El atributo `lang` es clave para la accesibilidad (lectores de pantalla) y buscadores.
* `<head>`: La mente de la página. Contiene metadatos, configuraciones, el título de la pestaña y enlaces a estilos. El usuario común no ve esto en la pantalla.
* `<meta charset="UTF-8">`: Declaración de codificación de caracteres. Evita que los acentos o la "ñ" se rompan y se vean como símbolos raros.
* `<body>`: El cuerpo visible de la página. Todo lo que pongamos acá adentro se renderizará en la pantalla.

### Etiquetas Semánticas Estructurales (HTML5)
* `<header>`: Contenedor para la cabecera de la página o de una sección (habitualmente lleva el logo y menú).
* `<nav>`: Bloque específico que contiene enlaces de navegación (menús).
* `<main>`: El contenido principal y único de este documento. No debe repetirse en otras páginas.
* `<section>`: Agrupador de contenido temático (ej. "Beneficios", "Contacto").
* `<footer>`: El pie de página (derechos de autor, links legales, redes).

## 4. Ejemplo simple
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estructura Base Semántica</title>
</head>
<body>
    <header>
        <h1>Mi Sitio Web</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section>
            <h2>Sección Principal</h2>
            <p>Contenido semántico e informativo.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2026 - Todos los derechos reservados.</p>
    </footer>
</body>
</html>