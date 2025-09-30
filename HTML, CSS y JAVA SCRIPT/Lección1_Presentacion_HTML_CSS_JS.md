# Introducción a HTML, CSS y JavaScript

## 1. ¿Qué es HTML?
HTML (HyperText Markup Language) es el lenguaje de marcado principal para crear páginas web. Define la estructura y el contenido de la web.

### Conceptos básicos de HTML
- **Etiquetas**: Elementos que definen partes de la página.
- **Atributos**: Propiedades adicionales de las etiquetas.
- **Estructura básica**:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi primera página</title>
  </head>
  <body>
    <h1>¡Hola, mundo!</h1>
    <p>Este es un párrafo.</p>
  </body>
</html>
```

---

## 2. ¿Qué es CSS?
CSS (Cascading Style Sheets) es el lenguaje que se utiliza para definir el estilo y la presentación de las páginas web.

### Conceptos básicos de CSS
- **Selectores**: Indican qué elementos se van a estilizar.
- **Propiedades**: Definen el aspecto visual (color, tamaño, etc.).
- **Sintaxis básica**:

```css
h1 {
  color: blue;
  font-size: 2em;
}
p {
  color: gray;
}
```

### Ejemplo de uso en HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 { color: blue; }
      p { color: gray; }
    </style>
  </head>
  <body>
    <h1>¡Hola, mundo!</h1>
    <p>Este es un párrafo estilizado.</p>
  </body>
</html>
```

---

## 3. ¿Qué es JavaScript?
JavaScript es el lenguaje de programación que permite agregar interactividad y dinamismo a las páginas web.

### Conceptos básicos de JavaScript
- **Variables**: Almacenan datos.
- **Funciones**: Agrupan instrucciones para ejecutar tareas.
- **Eventos**: Responden a acciones del usuario.

### Ejemplo de uso en HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <script>
      function saludar() {
        alert('¡Hola desde JavaScript!');
      }
    </script>
  </head>
  <body>
    <button onclick="saludar()">Saludar</button>
  </body>
</html>
```

---

## Resumen
- **HTML** estructura el contenido.
- **CSS** lo estiliza.
- **JavaScript** lo hace interactivo.

¡Estos tres lenguajes son la base del desarrollo web moderno!
