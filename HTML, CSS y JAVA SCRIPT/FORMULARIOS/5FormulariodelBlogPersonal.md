# Agregar un Formulario al Blog Perosnal

## Paso 1: Estructura HTML del Formulario
Vamos a añadir el formulario a tu archivo index.html, justo después de la sección de "Contacto", para que quede bien ubicado en la parte final del contenido.

### Inclusión del Formulario en index.html
- Localiza la etiqueta de cierre de tu sección de contacto (`</section>`) dentro del `<main>` y agrega el siguiente código justo después:

![Codigo html text_area ](assets/entrada_texto.png)

### Explicación de la Estructura HTML del Formulario
- `<section id="newsletter-signup">`: Creamos una nueva sección para el formulario. Esto es fundamental para la semántica del documento.

- `<h2>` y `<p>`: Título y descripción atractivos para motivar la suscripción.

- `<form action="#" method="POST" class="newsletter-form"`>: La etiqueta contenedora del formulario.

- `action="#"`: Indica dónde se enviarán los datos. Usamos # como marcador de posición, ya que para que funcione necesitarías un backend (JavaScript o un servidor).

- `method="POST"`: Indica cómo se envían los datos (ocultos en el cuerpo de la petición).

- `class="newsletter-form"`: Una clase específica para aplicar estilos.

- `<div class="form-group">`: Contenedores para agrupar las etiquetas (<label>) y los campos (<input>). Esto nos facilitará aplicar estilos de espaciado.

- `<label for="name">`: La etiqueta que describe el campo. El atributo for debe coincidir con el id del campo de entrada. Esto es crucial para la accesibilidad.

- `<input type="text" id="name" name="name" ... required>`: El campo de entrada de texto.

`type="text" o type="email"`: Define el tipo de dato que se espera. email activa el teclado de email en móviles.

- id y name: El id se usa con el label y el name es lo que usará el backend para identificar el dato.

- placeholder: Texto que aparece en el campo antes de que el usuario escriba.

- required: Un atributo HTML5 que impide el envío del formulario si el campo está vacío.

- `<button type="submit" class="subscribe-btn">`: El botón que activa el envío del formulario.
