# Programación en Java Script
## Funciones
Las funciones en JavaScript son bloques de código reutilizables que realizan tareas específicas. Se definen con la palabra clave function, un nombre, parámetros entre paréntesis y un conjunto de instrucciones entre llaves. Para que se ejecuten, deben ser "llamadas" por su nombre. Permiten encapsular lógica, organizar el código y evitar la repetición. 
### Componentes principales
- Palabra clave function: Indica que se está definiendo una función.
- Nombre de la función: Un identificador para llamar a la función. Es opcional en funciones anónimas.
- Paréntesis (): Contienen los parámetros (variables internas) que la función puede recibir.
- Llaves {}: Encierran el código que se ejecutará al llamar a la función.

## Uso de Funciones
### Creación de una función con parametro y argumentos

### Ejercicio 14.js:
Procedimiento:
- Crea una carpeta llamada **js**
- Crea un archivo llamado 14.js
- Enlaza tu archivo .js externo al html
-- Usa la etiqueta ```<script>``` con el atributo src
-- Escribe en el index.html lo siguiente:
  
  ```html
  <script src="js/14.js"></script>
  ```
  Realiza el siguiente ejercicio, los resultados podrás visualizarlo en la consola de ejecución de la página web. Para visualizarlo realiza lo siguiente:
  

```javascript 
function sumar(numero1, numero2){
    console.log(numero1+numero2);
}

sumar(10,5);     //invocación del metodo con argumentos
sumar(3,3);
sumar(200,300);

/*Expresión de una función*/
const sumar2= function(n1,n2){
    console.log(n1+n2);
}
sumar2(7,560);  /*Invocacionn del metodo sumar*/
```
## Funciones que retornan valores
Las funciones en JavaScript que retornan un valor utilizan la sentencia return para finalizar la ejecución de la función y devolver un resultado al código que la llamó. Este valor puede ser de cualquier tipo de dato, como números, cadenas, objetos o incluso otras funciones, y se puede guardar en una variable o usar directamente donde se espera un valor. 

### Ejercicio 15.js:
Procedimiento:
- Crea una carpeta llamada **js**
- Crea un archivo llamado 15.js
- Enlaza tu archivo .js externo al html
-- Usa la etiqueta ```<script>``` con el atributo src
-- Escribe en el index.html lo siguiente:
  
  ```html
  <script src="js/15.js"></script>
  ```
  Realiza el siguiente ejercicio, los resultados podrás visualizarlo en la consola de ejecución de la página web. Para visualizarlo realiza lo siguiente:
  

```javascript
function sumar(n1,n2){        //Definicion de una funcion llamada sumar
    return n1+n2;            //La funcion retornara el resultado de la suma de n1+n2
}

const resultado=sumar(2,3);    //Se invoca la funcion pasandole los valores 2 y 3
console.log(resultado);        //Mostramo en la consola el resultado de la invocacion

/*Segundo Ejemplo */
let total=0;
function agregarCarrito(precio){  //Definicion de la funcion agregarCarrito
    return total+=precio;        //la funcion retorna el resultado de la suma de total y precio
}

function calcularImpuesto(total){
    return 1.15*total;
}

total=agregarCarrito(200);   //Invocaciones de la funcion agregarCarrito
total=agregarCarrito(400);
total=agregarCarrito(600);

console.log(total);        //Mostramos en consola el total calculado

//Invocamos la funcion CalcularImpuesto, y el resultado que devuelve se asigna a la variable totalAPagar
const totalAPagar=calcularImpuesto(total);

//Mostramos en consola el Total a Pagar
console.log(`El total a pagar con impuestos es de: $${totalAPagar}`);
```
## Métodos de Propiedad

En JavaScript, los métodos de propiedad son funciones asociadas a un objeto, que representan las acciones que este puede realizar. Se diferencian de las propiedades (que son datos) y se definen como propiedades cuyo valor es una función. Algunos métodos de propiedad son los "getters" y "setters" (get y set) para controlar el acceso a las propiedades y métodos estáticos de clase. 

### Métodos de propiedad básicos
- Definición: Se definen dentro de un objeto como una propiedad y su valor es una función.
- Acceso: Se invocan usando la notación de punto (.), al igual que las propiedades.

### Ejercicio 16.js:
Procedimiento:
- Crea una carpeta llamada **js**
- Crea un archivo llamado 16.js
- Enlaza tu archivo .js externo al html

El siguiente ejercicio, simula un reproductor de musica.
```javascript

/*METODOS DE PROPIEDAD */

const reproductor={
    reproducir: function (id) {
        console.log(`Reproduciendo canción con el ID: ${id}`);
    },
    pausar:function(){
        console.log('Pausando...');
    }
}
reproductor.reproducir(3840); //invocacion del metodo reproducir
reproductor.pausar();   //invocacion del metodo pausar
```

Una segunda forma de especificar o crear una funcion para el objeto reproductor, es la siguiente:
Nota: Agrega el siguiente codigo al mismo archivo del ejercicio.

Escribimos:
- el nombre del objeto, despues un punto (.),
- seguido de esto el nombre del metodo,
- posteriormente el signo de =, parentesis para los parametros y
- finalmente el cuerpo de la funcion encerrados entre {}.
- 
```javascript
reproductor.borrarCancion=function(id){     
    console.log(`Elimando canción: ${id}`);
}
reproductor.borrarCancion(20);             //invocacion del metodo borrarCancion
```


