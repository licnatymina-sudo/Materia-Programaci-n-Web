# Añadiendo efecto scroll

Scroll snap es una propiedad de CSS que permite a los desarrolladores controlar el comportamiento de desplazamiento (scroll) en un contenedor, haciendo que se detenga automáticamente en puntos de "anclaje" predefinidos, lo que resulta en una experiencia de navegación más suave y organizada.

## Cómo funciona
- `scroll-snap-type:` Se aplica al contenedor principal (el que tiene el desplazamiento) y define si el ajuste se aplica en el eje x, y o ambos, y si es obligatorio o solo una sugerencia.
- `scroll-snap-align:` Se aplica a los elementos secundarios (los elementos dentro del contenedor) y determina en qué parte de ese elemento debe ajustarse el punto de anclaje, como start, end o center. 

Para aplicar un scroll snap a nuestro sitio web, accedemos a nuestro css, y en la etique html, escribimos los siguiente:

```css
html{
	font-size:%;
	box-sizing: border-box;
	scroll-nap-typs: y mandatory;
}
```

`scroll-nap-type:` y mandatory; nos va a permitir hacer scroll snap de arriba hacia abajo.

Ahora tendremos que definir a cada una de las secciones en las cuales queremos que se detenga el snap. En este caso en la sección servicios, navegación principal, y en la sección contacto en donde tenemos ubicado nuestro formulario.

Debajo de `html {   }`  escribimos:
```css
html{
	----
}
.servicios, 
.navegación-principal,
.formulario{
	  scroll-snap-align:center;
	  scroll-snap-stop: always;
}
```

El scroll-snap se aplicará a nuestra navegación principal y a nuestra sección de servicios.
- `scroll-snap-align: center;` alinea el centro de un elemento secundario al centro del contenedor de desplazamiento.
Con esto hemos finalizado nuestro proyecto de sitio web.

- `scroll-snap-stop: always;` evita que el desplazamiento rápido se "salte" elementos, forzando que se detenga y se ajuste en cada punto de anclaje definido por el contenedor padre.
  
Juntas, estas propiedades crean un desplazamiento de tipo carrusel donde cada elemento se centra perfectamente y el usuario se ve obligado a detenerse en cada uno, incluso al mover el scroll.

