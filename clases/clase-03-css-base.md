# Clase 3: CSS Base, Variables Globales y Arquitectura del Box Model

## Objetivos de la clase
* Sincronizar y configurar el repositorio de trabajo en un entorno local alternativo.
* Comprender el mecanismo de vinculación de hojas de estilo externas mediante la manipulación del bloque head.
* Implementar Custom Properties (Variables CSS) para centralizar la identidad visual de la aplicación.
* Dominar los componentes esenciales del Box Model (márgenes, rellenos, bordes y dimensiones) para estructurar contenedores, tablas financieras y formularios accesibles.

---

## 1. Configuración y Sincronización del Entorno Local

Para garantizar la portabilidad del proyecto fuera de entornos cloud, se ejecutó el flujo completo de clonación y verificación del repositorio en un entorno local:

```bash
# Clonación del repositorio remoto al almacenamiento local
git clone [https://github.com/popolo77/materia-2-html-css-figma-landing.git](https://github.com/popolo77/materia-2-html-css-figma-landing.git)

# Acceso al directorio raíz del proyecto
cd materia-2-html-css-figma-landing

# Verificación del estado del árbol de trabajo y la rama activa
git status
```

---

## 2. Vinculación de la Hoja de Estilos Externa

Para mantener la separación de responsabilidades (estructura y presentación), se creó un archivo independiente denominado `styles.css` dentro del directorio de la práctica. La conexión con el documento estructural se realizó insertando la etiqueta `link` antes del cierre del bloque `<head>` en el archivo `index.html`:

```html
<link rel="stylesheet" href="styles.css">
```

---

## 3. Prueba de Conectividad Inicial

Se aplicó un selector de tipo etiqueta para alterar de forma global las propiedades del documento y validar que el navegador interprete correctamente el archivo externo antes de avanzar con el diseño definitivo:

```css
body {
    background-color: #f0f2f5;
    color: #1c1e21;
    font-family: sans-serif;
}
```

---

## 4. Implementación de Variables CSS (Custom Properties)

Con el fin de asegurar la escalabilidad y consistencia de la interfaz de Uber Tracker, se definió un esquema de diseño centralizado utilizando el selector pseudo-clase `:root`. Esto expone las variables de color a todo el documento y permite modificaciones globales centralizadas:

```css
:root {
    --color-principal: #000000;      /* Negro oficial corporativo */
    --color-acento: #276ef1;         /* Azul de marca para acciones */
    --color-fondo: #f6f6f6;          /* Gris claro para el fondo general */
    --color-tarjeta: #ffffff;        /* Blanco para los contenedores */
    --color-texto: #333333;          /* Gris oscuro para el cuerpo de lectura */
    --color-exito: #05a357;          /* Verde para indicadores financieros */
}
```

---

## 5. Estructuración del Layout mediante el Box Model

Se aplicaron reglas de Box Model a las etiquetas estructurales de HTML5 para dar aire, legibilidad y jerarquía visual a la landing page, transformando las secciones sueltas en un formato de tarjetas profesionales:

```css
body {
    background-color: var(--color-fondo);
    color: var(--color-texto);
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: var(--color-principal);
    color: var(--color-tarjeta);
    padding: 20px;
    text-align: center;
}

main {
    max-width: 800px;
    margin: 20px auto;
    padding: 10px;
}

section {
    background-color: var(--color-tarjeta);
    margin-bottom: 25px;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

footer {
    background-color: var(--color-principal);
    color: var(--color-tarjeta);
    text-align: center;
    padding: 15px;
}
```

### Conceptos Técnicos Consolidados del Layout
* **margin: 20px auto;**: Centra horizontalmente el contenedor main dentro del viewport calculando automáticamente los márgenes laterales uniformes.
* **padding**: Introduce aire interno en las secciones para evitar que los elementos colisionen con los límites de la tarjeta.
* **box-shadow**: Aumenta la profundidad visual emulando un diseño de tarjetas en capas elevadas sobre el fondo general.

---

## 6. Diseño y Estilización Avanzada de Tablas de Datos

La tabla de "Simulación de Rendimiento Semanal" se formateó para presentar información financiera compleja de forma clara y ordenada, anulando los estilos por defecto del navegador:

```css
table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
}

th, td {
    padding: 12px 15px;
    text-align: left;
    border-bottom: 1px solid #e0e0e0;
}

th {
    background-color: var(--color-fondo);
    color: var(--color-principal);
    font-weight: bold;
    text-transform: uppercase;
    font-size: 0.85rem;
    letter-spacing: 0.5px;
}

tr:hover {
    background-color: #fafdff;
}
```

### Conceptos Técnicos Consolidados de Tablas
* **border-collapse: collapse;**: Fusiona los bordes adyacentes de las celdas en una única línea, eliminando la separación doble por defecto del navegador.
* **tr:hover**: Pseudo-clase de interacción que proporciona feedback visual inmediato al usuario al posicionar el cursor sobre una fila específica, mejorando el seguimiento visual de los datos estructurados.

---

## 7. Formateo y UX en Formularios de Captura de Datos

Se transformaron los controles nativos del formulario de contacto para brindar una experiencia de usuario fluida, estandarizada, responsiva y accesible:

```css
form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    max-width: 500px;
}

label {
    font-weight: bold;
    font-size: 0.9rem;
    color: var(--color-texto);
}

input, select, textarea {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 1rem;
    font-family: Arial, sans-serif;
    width: 100%;
    box-sizing: border-box;
}

input:focus, select:focus, textarea:focus {
    outline: none;
    border-color: var(--color-acento);
}

button {
    background-color: var(--color-acento);
    color: var(--color-tarjeta);
    padding: 12px;
    border: none;
    border-radius: 4px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    align-self: flex-start;
}

button:hover {
    background-color: #1a54c1;
}
```

### Conceptos Técnicos Consolidados de Formularios
* **box-sizing: border-box;**: Modifica el cálculo predeterminado del modelo de caja. Garantiza que el tamaño del elemento incluya el padding y el borde dentro del ancho total especificado, previniendo rupturas o desbordamientos en la tarjeta.
* **input:focus**: Cambia el color del contorno del elemento activo para denotar foco de forma clara, cumpliendo con las pautas de accesibilidad y diseño de interacción.

---

## 8. Trazabilidad de Cambios y Commits Realizados

Para mantener un historial limpio, coherente y defendible ante el tribunal evaluador de la UTN, se ejecutaron los siguientes comandos de resguardo al finalizar la sesión práctica:

```bash
git add .
git commit -m "feat: conectar hoja de estilos base, definir variables css y estilizar tablas y formularios"
git push origin main
```
