# Java Script

## ¿Qué es JavaScript?
JavaScript es un lenguaje de programación que permite crear contenido web interactivo y dinámico, trabajando junto con HTML y CSS para que las páginas web sean más que simple texto y gráficos estáticos. 

Es el lenguaje de la web.
- Añade interactividad a tus sitios web
- Desarrollo Front End.
- Desarrollo Back End.
- Desarrollo de aplicaciones Móviles y escritorio.

## JavaScript es un lenguaje maduro y estable
JavaScript tiene variables, funciones, estructuras de control, métodos lo cual lo hace un lenguaje de programación a diferencia de HTML o CSS

Esta lección te dará una introducción a JavaScript, realizarás una serie de ejercicios que te permitirán conoccer lo básico del lenguaje. Descarga previamente la carpeta IntroducciónJS, esta contiene: un archivo index.html y un archivo style.css los cuales te permitirán ejecutar cada uno de los ejercicios que iras realizando.

## Variables en JavaScript

### Tipos de declaraciones de variables
- let: Declara una variable local con alcance de bloque. Se puede reasignar a un nuevo valor.
  Ejemplo: let nombre = "Juan";
- const: Declara una constante, que no se puede reasignar después de su inicialización.
  Ejemplo: const pi = 3.14;
- var: Declara una variable con alcance de función o global. Se puede reasignar y redeclarar, aunque esto puede generar errores y no es la práctica recomendada en el código moderno.

### Ejercicio:
```javascript 
//Variables en Java Script

var producto='Audifonos gamer'; //Iniciar variable y asignar valor
console.log(producto)

var disponible; // Iniciamos variable pero sin valor
console.log(disponible)

producto=true; // reasignamos el valor de la variable
console.log(producto)

disponible=true;
console.log(disponible)

var producto1='computadora',
    disponible1=true,
    categoria='computadoras';
console.log(producto1,disponible1,categoria)

// Estilos de declaración para las variables
var nom_producto='Monitor HD'; //underscore
var nombre='Monitor HD'; //Camelcase
var NombreProducto='Monitor HD'; //pascal case
console.log(NOMBREPRODUCTO); //Observa que no se mostrara nada, ya que no hay ninguna variable
                            //declarada como NOMBREPRODUCTO todo en mayuscula como la
                            //la estamos especificando en el console.

```
##
