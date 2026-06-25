# Tema 02: Formularios, Tablas y Metadatos

## 1. Objetivo
Aprender a construir estructuras de captura de datos (formularios) interactivas, organizar información estructurada (tablas) y configurar los metadatos esenciales para optimizar el SEO y la accesibilidad de nuestra aplicación Uber Tracker.

## 2. Componentes de un Formulario
Los formularios permiten que el usuario interactúe y envíe información a nuestra app. Componentes clave:
* `<form>`: Contenedor principal. Define a dónde se envían los datos.
* `<label>`: La etiqueta de texto vinculada a un control. Es obligatoria para la accesibilidad.
* `<input>`: Campo de entrada de datos. Cambia según su atributo `type` (`text`, `email`, `number`, `password`).
* `<textarea>`: Campo de texto multilínea para mensajes extensos.
* `<select>` y `<option>`: Menús desplegables de opciones.
* `<button type="submit">`: El gatillo que procesa y envía el formulario.

## 3. SEO y Metadatos (El <head>)
Los metadatos le dicen a los motores de búsqueda (como Google) de qué trata la página:
* `<meta name="description" content="...">`: El resumen que aparece en los resultados de búsqueda.
* `<meta name="keywords" content="...">`: Palabras clave del sitio.