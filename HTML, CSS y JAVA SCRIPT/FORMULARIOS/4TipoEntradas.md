# Tipos de Entrada HTML
Estos son los diferentes tipos de entrada que puedes utilizar en HTML:

```HTML
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="datetime-local">
<input type="email">
<input type="file">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<input type="radio">
<input type="range">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```
**Consejo: El valor predeterminado del type atributo es "texto".**

## Tipo de entrada Texto
`<input type="text">` define un campo de entrada de texto de una sola línea :

Ejemplo
```HTML
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>
```
![Codigo html text_area ](assets/entrada_texto.png)

## Tipo de entrada Contraseña
`<input type="password">` define un campo de contraseña :

**Ejemplo**
```HTML
<form>
  <label for="username">Username:</label><br>
  <input type="text" id="username" name="username"><br>
  <label for="pwd">Password:</label><br>
  <input type="password" id="pwd" name="pwd">
</form>
```
![Codigo html text_area ](assets/entrada_password.png)

**Los caracteres en un campo de contraseña están enmascarados (se muestran como asteriscos o círculos).**

## Tipo de entrada Enviar
`<input type="submit">` define un botón para enviar datos del formulario a un controlador de formulario .

El controlador de formulario normalmente es una página de servidor con un script para procesar datos de entrada.

El controlador del formulario se especifica en el action atributo del formulario:

**Ejemplo**
```HTML
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>
```
![Codigo html text_area ](assets/Entrada_enviar.png)

Si omite el atributo de valor del botón Enviar, el botón obtendrá un texto predeterminado:

**Ejemplo**
```HTML
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit">
</form>
```

## Tipo de entrada Restablecer
`<input type="reset">`define un botón de reinicio que restablecerá todos los valores del formulario a sus valores predeterminados:

**Ejemplo**
```HTML
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
  <input type="reset" value="Reset">
</form>
```

![Codigo html text_area ](assets/entrada_reset.png)

## Tipo de entrada Radio
`<input type="radio">` define un botón de opción .

Los botones de opción permiten al usuario seleccionar SÓLO UNA de un número limitado de opciones:

**Ejemplo**
```HTML
<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>
```

Así es como se mostrará el código HTML anterior en un navegador:
![Codigo html text_area ](assets/entrada_radio.png)

## Casilla de verificación de tipo de entrada
`<input type="checkbox">`define una casilla de verificación .

Las casillas de verificación permiten al usuario seleccionar CERO o MÁS opciones de un número limitado de opciones.

**Ejemplo**
```HTML
<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label>
</form>
```

Así es como se mostrará el código HTML anterior en un navegador:

![Codigo html text_area ](assets/entrada_casilla.png)

## Botón de tipo de entrada
`<input type="button">` define un botón :

**Ejemplo**
`<input type="button" onclick="alert('Hello World!')" value="Click Me!">`

Así es como se mostrará el código HTML anterior en un navegador:
![Codigo html text_area ](assets/entrada_boton.png)


## Tipo de entrada Color
Se `<input type="color">`utiliza para campos de entrada que deben contener un color.

Dependiendo de la compatibilidad del navegador, puede aparecer un selector de color en el campo de entrada.

**Ejemplo**
```HTML
<form>
  <label for="favcolor">Select your favorite color:</label>
  <input type="color" id="favcolor" name="favcolor">
</form>
```
![Codigo html text_area ](assets/entrada_color.png)
