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
![Codigo html Ejercicio 1 ](sitio web/imagenes/responsive1.png)
EN EL ARCHIVO CSS..
La clase contenedor debe tener las siguientes propiedades:
```css
	.contenedor{
		max-with:120rem;
		margin:0 auto;
	}
```
### PASO C. Modificar la clase navegacion
EN EL ARCHIVO CSS..
Modificamos la clase .navegacion y agregamos las siguientes 2 lineas:
```css
	.navegacion-principal a {
		display:block;
	    text-align:center;
	..
	}
```
### PASO D. Mover la propiedad justyfy-content
EN EL ARCHIVO CSS..
Ahora movemos el **justyfy-cotent: space-between** ubicado en **.navegacion-principal** al **@media**, esto es para permitir adaptarse en este tipo de dispositivo de 768px
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






