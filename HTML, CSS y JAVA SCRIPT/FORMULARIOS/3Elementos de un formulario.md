# Elementos de formulario HTML
Este capítulo describe todos los diferentes elementos de formulario HTML.

# Los elementos HTML <form>
El elemento HTML <form>puede contener uno o más de los siguientes elementos de formulario:

- `<input>`
- `<label>`
- `<select>`
- `<textarea>`
- `<button>`
- `<fieldset>`
- `<legend>`
- `<datalist>`
- `<output>`
- `<option>`
- `<optgroup>`

## El elemento `<input>`
Uno de los elementos de formulario más utilizados es el elemento `<input>`.

El elemento `<input>` se puede mostrar de varias maneras, dependiendo del type atributo.

Ejemplo
```HTML
<label for="fname">Primer nombre:</label>
<input type="text" id="fname" name="fname">
```
Todos los diferentes valores del type atributo se tratan en el siguiente capítulo: Tipos de entrada HTML .

## El elemento `<label>`
- El elemento `<label>` define una etiqueta para varios elementos de formulario.

- El elemento `<label>` es útil para los usuarios de lectores de pantalla, porque el lector de pantalla leerá en voz alta la etiqueta cuando el usuario se centre en el elemento de entrada.

- El elemento `<label>` también ayuda a los usuarios que tienen dificultades para hacer clic en regiones muy pequeñas (como botones de opción o casillas de verificación), porque cuando el usuario hace clic en el texto dentro del <label>elemento, alterna el botón de opción o la casilla de verificación.

- El atributo for  de la etiqueta `<label>` debe ser igual al idatributo del <input> elemento para unirlos.

## El elemento `<select>`
El elemento `<select>` define una lista desplegable:

**Ejemplo**
``` HTML
<label for="cars">elecciona un auto:</label>
<select id="cars" name="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select>
```
- El elemento `<option>` define una opción que se puede seleccionar.

- De forma predeterminada, se selecciona el primer elemento de la lista desplegable.

- Para definir una opción preseleccionada, agregue el selectedatributo a la opción:

**Ejemplo**
`<option value="fiat" selected>Fiat</option>`

**Valores visibles:**
Utilice el atributo **size** para especificar el número de valores visibles:

**Ejemplo**
```HTML
<label for="cars">elecciona un auto:</label>
<select id="cars" name="cars" size="3">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select>
```
Permitir selecciones múltiples:
Utilice el atributo **multiple** para permitir que el usuario seleccione más de un valor:

**Ejemplo**
```HTML
<label for="cars">Selecciona un auto:</label>
<select id="cars" name="cars" size="4" multiple>
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select>
```

## El elemento `<textarea>`
El elemento `<textarea>` define un campo de entrada de varias líneas (un área de texto):

**Ejemplo**
```HTML
<textarea name="message" rows="10" cols="30">
El gato juega en el jardin
</textarea>
```
- El atributo rows especifica el número visible de líneas en un área de texto.

- El atributo cols especifica el ancho visible de un área de texto.

Así es como se mostrará el código HTML anterior en un navegador:

![Codigo html text_area ](assets/formulario/text_area_1.png)

