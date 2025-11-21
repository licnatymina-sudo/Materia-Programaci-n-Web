# 3er Avance de construcción del Sitio Web Freelancer

## 1. Degradados con CSS

### A. Agregar un degradado con linear-gradient

Se agregará un color de fondo aplicando degradado para nuestro sitio web. Dado que será para toco el sitio, la propiedad será agregada en la etiqueta **body**.
Para acceder al degradado o gradient en css utilizaremos la propiedad **background-image**, aunque no se trata de una imagen como tal se utiliza esa propiedad. Utilizamos la sintaxis de `linear-gradient (dirección, color1, color2, ...);`

- **dirección:** Especifica la dirección del degradado.
- - **Palabras clave:** Usa palabras como `to top, to bottom, to left, to right,` o combinaciones como `to top right`. Si no se especifica, el valor predeterminado es to bottom.
- **color1, color2, ...:** Al menos dos colores son obligatorios. Puedes usar nombres de color, valores hexadecimales, RGB, etc.
- - **color-stop opcional:** Puedes añadir un porcentaje o longitud (% o px) para indicar dónde debe comenzar un color o dónde debe completarse una transición de color.

En nuestra página el degradado, la dirección va de abajo hacia arriba, entonces se utilizará la palabra clave `to top`. 
Como va de abajo hacia arriba, primero se le pasa con que color iniciará el degradado, y añadimos en que porcentaje o longitud comenzará el color. en segundo lugar, se agregará el color con el que terminará el degradado y el porcentaje en el que terminará.
```css 
body
{
	…….
  background-image: linear-gradient( to top, var(--grisclaro) 0%, var(--blanco) 100%);
}
```
Dado que no tenemos agregado el color gris claro en nuestra paleta de colores agrégalo.
```css 
:root{
  -----
  -----
  --grisclaro:#DFE9F3;
}
```
Observa como se ha agregado el degradado, has tus pruebas con diferentes colores, para que veas el cambio.

### B. Centrar el contenido principal
Aplicaremos estilos al contenido principal (main), para esto reutilizaremos la clase contenedor, cuyo css ya se ha definido, en tu index.html agrégalo a la sección main, como se describe a continuación
```css
<main class=”contenedor”>
	<h2>Mis servicios</h2>
	….
</main>
```

## 2. Sombras con css

Utiliza el siguiente código para agregar una sombra a nuestro contenedor principal.
```css
.sombra {
    box-shadow: 0px 5px 15px 0px rgba(112,112,112,0.48);
    background-color: var(--blanco); /*se le agrega un fondo blanco*/
    padding: 2rem; /*agregamos un padding*/
    border-radius: 1rem; /*permitirá darnos un border redondeado*/
}
```
Ya definidos los estilos para la sombra, ahora agrega esta al contenedor principal (main):
```css
<main class=”contenedor sombra”>
	<h2>Mis servicios</h2>
	….
</main>
```


Vamos a agregar un poco de separación en la imagen de fondo que se encuentra en la clase .hero, entonces escribimos lo siguiente:
```css

.hero{
	--
	Margin-bottom:2rem;
}
```
Esto nos permitirá separar el contenido de la clase .hero con el contenido principal.

![SitioWeb](imagenes/sombra_sitioW.png)

## 3. Usar CSS grid, para nuestra sección de servicios

Como primer paso vamos a agregar un contenerdor para nuestras 3 secciones creadas para nuestros servicios, escribiendo lo siguiente:
```css
<main class="contenedor sombra">
    <h2>Mis Servicios</h2>	
	<div class=”servicios”>
		<section> ...
		</section>
		<section> ...
		</section>
		<section> ...
		</section>
	</div>
</main>
```
Cerramos el `</div>` después del cierre de la ultima sección, y justo antes del cierre del `</main>`.

### A. Css Grid
- **CSS Grid** es un sistema de maquetación bidimensional para CSS que permite diseñar páginas web dividiéndolas en filas y columnas, facilitando la creación de estructuras complejas de forma más sencilla y coherente.
- Se activa aplicando la propiedad display: grid a un elemento padre, lo que convierte a sus hijos en elementos de la cuadrícula que pueden ser posicionados y organizados de manera precisa.
Ahora vamos a nuestro css, y crearemos un grid para nuestra clase **.servicios**
```css
.servicios{
	display:grid;
	grid-template-columns:33.3% 33.3% 33.3%;
	/*grid-template-columns: repeat(3, 1fr);  realiza lo mismo que la linea anterior*/
}
```
![SitioWeb](imagenes/grid_sitioW.png)

- `grid-template-columns:33.3% 33.3% 33.3%;` esta línea nos permite crear 3 columnas en nuestro grid, cada una con un tamaño del 33.3% del 100% de nuestro contenedor actual. Otra forma más simplificada de crear esas tres columnas es con el código: `grid-template-columns: 1fr 1fr 1fr;` donde fr significa fracción, Lo que quiere decir que cada columna tendrá una fracción del entero que representa al contenedor, y dado que agregamos 1fr 3 veces, son en total 3 fracciones. Asi que `1fr =33.3%`
- `grid-template-columns: repeat(3, 1fr);`  Otra manera de crear 3 columnas con el mismo tamaño es usando `repeat,(3, 1fr)` donde especificamos que se crearan 3 columnas con un tamaño de 1 fracción para cada columna.

Visualiza tu sitio web, y notaras que en dispositivos mas pequeños se mantienen las 3 columnas y se ve amontonado.

![SitioWeb](imagenes/grid_sitioResponsive.png)

Para corregir esto, agregaremos un **@media**, para que las 3 columnas se aplique solo en dispositivos de **768px**. Y edianuestro código quedará así:
```css
@media(min-width: 768px){
	.servicios{
		display:grid;
		grid-template-columns:33.3% 33.3% 33.3%;
}
```

Ahora agregamos una separación entre columnas, para que el contenido no este pegado, esto lo hacemos con la propiedad `column-gap: 1rem;`
```css
@media(min-width: 768px){
	.servicios{
		display:grid;
		grid-template-columns:33.3% 33.3% 33.3%;
		column-gap: 1rem;
}
```
![SitioWeb](imagenes/grid_sitiosResponsive2.png)
