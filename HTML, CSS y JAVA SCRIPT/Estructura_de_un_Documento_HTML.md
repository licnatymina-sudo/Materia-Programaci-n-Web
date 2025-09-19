# Estructura de un Documento HTML

---

## 1. ¿Qué es la Estructura de un Documento HTML?

La estructura de un documento HTML es como el esqueleto de un ser vivo. Proporciona el orden y la jerarquía necesarios para que un navegador entienda, interprete y muestre correctamente el contenido de una página web. Cada elemento y etiqueta tiene un propósito específico y un lugar en esta jerarquía. Si el esqueleto está bien formado, la página se verá y funcionará como se espera.

---

## 2. Componentes Fundamentales

Todo documento HTML5 comienza con una declaración de tipo de documento y está envuelto en etiquetas principales que lo dividen en dos secciones esenciales: la cabeza (`<head>`) y el cuerpo (`<body>`).

### Ejemplo básico de estructura HTML
```html
<!DOCTYPE html>
<html lang="es">
<head>
    </head>
<body>
    </body>
</html>
```
###
- <!DOCTYPE html>: Esta es la primera línea y le dice al navegador que el documento es de tipo HTML5. Es una declaración obligatoria.
- <html lang="es">: Esta es la etiqueta raíz de todo el documento. Contiene todos los demás elementos. El atributo lang="es" indica que el idioma principal del contenido es español, lo cual es útil para la accesibilidad y los motores de búsqueda.
- <head>: La "cabeza" del documento. No contiene contenido visible para el usuario. Su propósito es incluir metadatos e información para el navegador, como el título de la página, la vinculación a hojas de estilo CSS y archivos JavaScript, y la configuración de caracteres.
- <body>: El "cuerpo" del documento. Aquí es donde va todo el contenido que los usuarios ven en su navegador: textos, imágenes, videos, enlaces, tablas, etc.
---

## 3. Elementos dentro del <head>

Aunque no es visible, el <head> es crucial para el buen funcionamiento de la página. Los elementos más comunes que encontrarás aquí son:

- <meta charset="UTF-8">: Define la codificación de caracteres del documento. UTF-8 es el estándar global y asegura que el navegador pueda mostrar correctamente tildes, la letra "ñ" y otros caracteres especiales sin problemas.

- <meta name="viewport" content="width=device-width, initial-scale=1.0">: Esto es fundamental para el diseño web responsivo. Le dice al navegador que la página debe ajustarse al ancho del dispositivo (width=device-width) y que no debe tener un zoom inicial (initial-scale=1.0).

- <title>: Define el título que se muestra en la pestaña del navegador o en la barra de título de la ventana. Es muy importante para el SEO (Optimización para Motores de Búsqueda).

- <link rel="stylesheet" href="styles.css">: Vincula una hoja de estilos externa (styles.css) para darle apariencia a la página. rel="stylesheet" especifica la relación del archivo.

- <script src="main.js"></script>: Vincula un archivo JavaScript externo. Puede ir en el <head>, aunque a menudo se coloca al final del <body> para asegurar que el contenido HTML se cargue antes de ejecutar el script

## 4. Etiquetas Semánticas y de Contenido en el <body>

Dentro del <body>, utilizamos etiquetas para estructurar el contenido de manera significativa. Esto se conoce como HTML semántico, que no solo le da estilo al texto, sino que describe el propósito de cada elemento.

- Encabezados (<h1> a <h6>): Definen la jerarquía de los títulos. <h1> es el más importante y solo debe haber uno por página, mientras que <h6> es el menos importante.
- Párrafos (<p>): Se utiliza para bloques de texto.
- Enlaces (<a>): Se usa para crear hipervínculos a otras páginas o recursos.
- Listas (<ul>, <ol>, <li>): Se usan para crear listas. <ul> es para listas no ordenadas (con viñetas) y <ol> para listas ordenadas (con números o letras). Cada elemento de la lista va dentro de una etiqueta <li>.
- Secciones Semánticas:
-   <header>: Contenedor para el encabezado de la página o de una sección. A menudo contiene la navegación y el logo.
-   <nav>: Contiene los enlaces de navegación de la página.
-   <main>: El contenido principal y único de la página.
-   <article>: Una pieza de contenido independiente, como una entrada de blog o un artículo de noticias.
-   <section>: Una sección temática de la página, como "Sobre Mí" o "Habilidades".
-   <footer>: El pie de página. Contiene información como derechos de autor o enlaces de contacto.

Comprender esta estructura es el primer paso para construir una página web funcional y bien organizada.
