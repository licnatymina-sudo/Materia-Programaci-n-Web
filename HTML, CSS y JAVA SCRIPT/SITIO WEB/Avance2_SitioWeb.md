# Construcciónn del Sitio Web Freelancer

## 1. Introducción a Responsive Web Design
El término "responsive" en diseño web se refiere a la capacidad de un sitio web para adaptarse automáticamente a cualquier tamaño de pantalla y dispositivo (ordenador, tablet, móvil) y ofrecer una experiencia de usuario óptima.
Las media queries son una funcionalidad de CSS que permite aplicar estilos CSS condicionalmente según las características del dispositivo, como el ancho de la pantalla, la resolución o el tipo de medio 

### PASO A. Añadiendo los media Queries
EN EL ARCHIVO CSS escribe:
```css
/*Agregamos el media query Para una tableta*/
@media(min-width:768px){
	.navegacion-principal{
		flex-direction:row;
	}
}
```
Esto permitira adaptar la barra de navegación en dispositivos con un tamaño de 768px.

### PASO B. Modificar la clase contenedor.
Observa que la barra de navegación aun no se adapta a otros dispositivos con pantallas mas pequeñas.
![SitioWeb](imagenes/responsive1.png)

En el archivo CSS..
La clase contenedor debe tener las siguientes propiedades:
```css
	.contenedor{
		max-with:120rem;
		margin:0 auto;
	}
```
Con el cambio anterior puedes notar como la barra de navegación ya se adapta a los distintos tamaño de pantalla.
![SitioWeb](imagenes/responsive2.png)

**Nota:** Para que puedas ver tu sitio web en distintos tipos de dispositivos e ir verificando tu diseño responsivo, puedes utilizar la aplicación **Responsively App**, puedes descargar la aplicación en el siguiente enlace: https://responsively.app/
Una vez decargado, solo escribe la ubicación de tu proyecto en la barra de direccion de la aplicación, y podrás ir visualizando tu proyecto conforme vayas realizando las modificaciones.

### PASO C. Modificar la clase navegacion
EN EL ARCHIVO CSS..
Modificamos la clase .navegacion-principal y agregamos las siguientes 2 lineas:
```css
	.navegacion-principal a {
		display:block;
	    text-align:center;
		display: flex;
    	justify-content:space-between;
	..
	}
```
### PASO D. Mover la propiedad justyfy-content
EN EL ARCHIVO CSS..
Ahora movemos el **justyfy-cotent: space-between** ubicado en **.navegacion-principal** al **@media**, esto es para permitir adaptarse en dispositivos de 768px
```css
	@media(min-width:768px{
	.navegacion-principal{
		Flex-direction:row;
		justity-content:space-between;
		}
	}
```
## 2. Imagenes con CSS
Agregaremos una imagen debajo de la barra de navegación, y la pondremos de fondo, agregandole un estilos

### PASO A: Crear la clase hero
Crearemos una clase en la etiqueta **`<section>`**, llamada **hero**, para poder darle estilos a esta sección. 
Vaya al codigo HTML, y agregue la clase, la seccion debe verse como en el siguiente codigo:
```html
	<section class="hero">
	        <h2>Diseño y dessarrollo Web Freelancer</h2>
	        <svg
```
### PASO B. Agregar estilos
Ahora agregamos estilos a la clase **hero**, colocaremos de fondo la imagen hero.jpg.
Para esto primero eliminamos la imagen que tenemos agregada, para quedarnos solo con la que estará de fondo.
```html
    </div>
  	  <img src="hero.jpg"> <- Elimine esta linea
  	  <!--section-->
	  <section class="hero">
```
Ahora agregue los estilos
```css
.hero{
    background-image: url(../hero.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
```
-- Agregamos `background-image: url(../hero.jpg);` para especificar una imagen de fondo para la **sección** de la clase **hero**.
-- Debido a que la imagen se repite en pantallas grandes, utilizaremos `background-repeat: no-repeat;`
-- Ahora podrás ver que la imagen en algunos dispositivos no abarca toda la pantalla, utilizamos la propiedad: `background-size: cover;` y la imagen tomara todo el ancho disponible

## Diseño de Caja - Box Model
“Una de las cosas que menos me gustan del diseño con CSS es la relación entre el ancho y el relleno. Estás ocupado definiendo anchos para que coincidan con la cuadrícula o las proporciones generales de las columnas, y luego empiezas a añadir texto, lo que requiere definir el relleno para esos recuadros. Y, ¡oh sorpresa!, ahora estás restando píxeles al ancho original para que el recuadro no se expanda.” (**Paul Irlandes**)

Para evitar estar ajustando el tamaño del elemento por los padding y border que le podamos agregar, como solución podemos aplicar el siguiente código css proporcionado por **Paul Irlandes**, desarrollador de Google.

Agrega a la etiqueta html en el archivo css
```css
html{
	Box-sizing:border-box;
}
/*Y agrega el siguiente código después de la etiquema html en el css.*/

*,*:before, *:after{
	Box-sizing:inherit;
	}
```
Este código permitirá seleccionar todos los elementos html, y aplicar el box-sizing, lo que permitirá que se mantenga el tamaño del elemento aunque se agreguen otras propiedades como el padding o border.

## Agregar una sombra a la imagen
Para darle un estilo de sobra a la imagen de fondo que se muestra en nuestro sitio web, tal y como se muestra en la siguiente imagen, debemos realizar lo siguiente:
![SitioWeb](imagenes/responsive2.png)
Primero agregaremos en contenedor div en nuestra etiqueta <section class=”hero”> en nuestro html, esto es para poder manipular mejor la imagen que se coloca de fondo y los elementos de la sección.

<section class=hero>
<div class=”contenido-hero”>
… aquí agregamos el contenido del section
</div>
</section>

Ahora en el css, agregamos los siguientes estilos:

.contenido-hero{

Background-color:rgba(0,0,0,.7) /*Definimos el color negro con un .7 de trasparencia*/
Width:100%;  /*con un ancho del 100% dentro del contenedor div*/
Height:100%; /*con un alto del 100%*/
}
Agregamos las propiedades:
Position:relative;   en la clase .hero{ - -} ya que fungirá como el elemento hijo, para que su posición sea en base a la posición que tenga el elemento o clase .hero.
Position: absolute;  en la clase .contenido-hero ya que fungirá como el elemento padre, y su posición determinará la del elemento de la clase .hero.
.hero{
Position:relative;
}
.contenido-hero{
	Position:absolute;
Background-color:rgba(0,0,0,.7) /*Definimos el color negro con un .7 de trasparencia*/
Width:100%;  /*con un ancho del 100% dentro del contenedor div*/
Height:100% /*con un alto del 100%*/





