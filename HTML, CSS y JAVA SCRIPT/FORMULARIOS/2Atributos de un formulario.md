### Atributos de formulario HTML
Este lección describe los diferentes atributos del `<form>`elemento HTML.

## El atributo de acción
- El actionatributo define la acción que se realizará cuando se envía el formulario.

- Normalmente, los datos del formulario se envían a un archivo en el servidor cuando el usuario hace clic en el botón enviar.

En el siguiente ejemplo, los datos del formulario se envían a un archivo llamado "action_page.php". Este archivo contiene un script del servidor que gestiona los datos del formulario:

**Ejemplo**
- Al enviar, envíe los datos del formulario a "action_page.php":
```HTML
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>
```
**Consejo:** si se omite el actionatributo, la acción se establece en la página actual.

## El atributo objetivo
- El targetatributo especifica dónde mostrar la respuesta que se recibe después de enviar el formulario.

- El targetatributo puede tener uno de los siguientes valores:
|-------------------|----------------------------------------------------------|
|      Value	      |              Description                                 | 
|-------------------|----------------------------------------------------------|
|_blank           	|The response is displayed in a new window or tab          |
|_self	            |The response is displayed in the current window           |
|_parent          	|The response is displayed in the parent frame             |
|_top	              |The response is displayed in the full body of the window  |
|framename         	|The response is displayed in a named iframe               |
|-------------------|----------------------------------------------------------|

El valor predeterminado es , _selflo que significa que la respuesta se abrirá en la ventana actual.

**Ejemplo**
Aquí, el resultado enviado se abrirá en una nueva pestaña del navegador:

`<form action="/action_page.php" target="_blank">`

## El atributo de método
- El atributo method  especifica el método HTTP que se utilizará al enviar los datos del formulario.
- Los datos del formulario se pueden enviar como variables de URL (con method="get") o como transacciones posteriores HTTP (con method="post").
- El método HTTP predeterminado al enviar datos del formulario es GET. 

**Ejemplo**
Este ejemplo utiliza el método GET al enviar los datos del formulario:

`<form action="/action_page.php" method="get">`

**Ejemplo**
Este ejemplo utiliza el método POST al enviar los datos del formulario:

`<form action="/action_page.php" method="post">`

**Notas sobre GET:**

- Añade los datos del formulario a la URL, en pares nombre/valor
- ¡NUNCA use GET para enviar datos confidenciales! (¡Los datos del formulario enviado son visibles en la URL!)
- La longitud de una URL es limitada (2048 caracteres)
- Útil para envíos de formularios en los que un usuario desea marcar el resultado como favorito.
- GET es bueno para datos no seguros, como cadenas de consulta en Google

**Notas sobre la POST:**

- Añade los datos del formulario dentro del cuerpo de la solicitud HTTP (los datos del formulario enviado no se muestran en la URL)
- POST no tiene limitaciones de tamaño y se puede utilizar para enviar grandes cantidades de datos.
Los envíos de formularios con POST no se pueden marcar como favoritos
Consejo: ¡ Utilice siempre POST si los datos del formulario contienen información confidencial o personal!
