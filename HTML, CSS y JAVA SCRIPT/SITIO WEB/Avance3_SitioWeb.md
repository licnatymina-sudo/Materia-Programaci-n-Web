# 3er Avance de construcción del Sitio Web Freelancer

## 1. Degradados con CSS

### Agregar un degradado con linear-gradient
Se agregará un color de fondo aplicando degradado para nuestro sitio web. Dado que será para toco el sitio, la propiedad será agregada en la etiqueta **body**.
Para acceder al degradado o gradient en css utilizaremos la propiedad **background-image**, aunque no se trata de una imagen como tal se utiliza esa propiedad. Utilizamos la sintaxis de `linear-gradient (dirección, color1, color2, ...);`
- dirección: Especifica la dirección del degradado.N EL ARCHIVO CSS escribe:
- Palabras clave: Usa palabras como to top, to bottom, to left, to right, o combinaciones como to top right. Si no se especifica, el valor predeterminado es to bottom.
- color1, color2, ...: Al menos dos colores son obligatorios. Puedes usar nombres de color, valores hexadecimales, RGB, etc.
- color-stop opcional: Puedes añadir un porcentaje o longitud (% o px) para indicar dónde debe comenzar un color o dónde debe completarse una transición de color.

En nuestra página el degradado, la dirección va de abajo hacia arriba, entonces se utilizará la palabra clave to top. 
Como va de abajo hacia arriba, primero se le pasa con que color iniciará el degradado, y añadimos en que porcentaje o longitud comenzará el color. en segundo lugar, se agregará el color con el que terminará el degradado y el porcentaje en el que terminará.
``` 
body
{
	…….
  background-image: linear-gradient( to top, var(--grisclaro) 0%, var(--blanco) 100%);
}
```
Dado que no tenemos agregado el color gris claro en nuestra paleta de colores agrégalo.
```
:root{
  -----
  -----
  --grisclaro:#DFE9F3;
}
```
Observa como se ha agregado el degradado, has tus pruebas con diferentes colores, para que veas el cambio.

