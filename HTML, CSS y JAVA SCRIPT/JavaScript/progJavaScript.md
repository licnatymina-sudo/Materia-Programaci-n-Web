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
- En la carpeta js crea un archivo llamado 14.js
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
  
```javascript
reproductor.borrarCancion=function(id){     
    console.log(`Elimando canción: ${id}`);
}
reproductor.borrarCancion(20);             //invocacion del metodo borrarCancion
```
## Arrow Function
Las arrow functions o funciones de flecha son una forma más concisa de escribir funciones en JavaScript, introducidas en ES6, que permiten simplificar la sintaxis y mejorar la legibilidad del código. Su característica principal es la sintaxis reducida, que omite palabras clave como function y return en muchos casos, y manejan el this de una forma diferente a las funciones tradicionales.

### Características principales
Sintaxis concisa:
- Sin parámetros: () => { ... }
- Un solo parámetro: nombre => 'Hola ' + nombre (los paréntesis alrededor del parámetro son opcionales)
- Varios parámetros: (a, b) => a + b
- Retorno implícito: Cuando el cuerpo de la función es una sola expresión, se puede omitir la palabra clave return y las llaves. El resultado de la expresión se devuelve automáticamente.
-- Ejemplo: const sumar = (a, b) => a + b; es equivalente a const sumar = function(a, b) { return a + b; }.
- Retorno explícito: Si la función tiene más de una línea o necesita ejecutar varias sentencias, se utilizan llaves {} y se debe usar return explícitamente.
-- Ejemplo: const sumar = (a, b) => { const resultado = a + b; return resultado; }.
- Manejo del this: Las arrow functions no tienen su propio enlace a this y capturan el this del contexto circundante. Esto las hace ideales para callbacks y las diferencia de las funciones tradicionales, que tienen su propio valor de this.
- Limitaciones: No son adecuadas en todas las situaciones, como cuando se usan como métodos de objeto o como constructores, debido a su manejo particular de this y su falta de sus propias palabras clave arguments

### Ejercicio 17.js:
Procedimiento:
- Crea una carpeta llamada **js**
- Crea un archivo llamado 17.js
- Enlaza tu archivo .js externo al html
- Crea el siguiente ejercicio paso a paso, y verifica su resultado en la consola.

Recuerda que:
-- ARROWS FUNCTION = Funciones Flechas
-- Es otra forma de declarar las funciones
-- Las declaraciones son mas cortas

Crea la siguiente función
```javascript

const sumar= function(n1,n2){
    console.log(n1+n2);
}

sumar(7,560);  /*Invocacionn del metodo sumar*/
```
- En el siguiente código tenemos la misma funcion,, pero con otro nombre
- Aplicaremos Arrow function
-- Paso1: omite la palabra function
-- Paso2: Despues de cerrrar el parentesis del parametro agrega =>
-- Paso2: Si tu funcion solo tiene una linea en su cuerpo, puedes omitir las llaves

```Javascript
const sumar2= (n1,n2)=>console.log(n1+n2);

sumar2(7,560);       //invoca el arrow function, y muestralo en consola
                    //observa que el resultado es lo mismo pero con menos código

//Crearemos un 2do arrow Function, cuya estructura general es la siguiente:
/*const aprendiendo=()=>{

}*/

const aprendiendo=(tecnologia)=>{
    console.log(`Aprendiendo ${tecnologia}`);
}
aprendiendo('JavaScript');
```

- copia el codigo del ejercicio 13, Carrito de compras y pegalo en este ejercicio
- Iremos convirtiendo en Arrow Function las funciones que tenemos en el ejercicio

```javascript
const meses=['Enero','Febrero','Marzo','Abril','Mayo'];

const carrito=[
    {nombre:'Monitor 20 Pulgadas', precio:500},
    {nombre:'Television 50 pulgadas', precio:8000},
    {nombre:'Tableta 9 Pulgadas', precio:5000},
    {nombre:'Celular', precio:7000},
    {nombre:'Bocinas', precio:500},
    {nombre:'Laptop', precio:21000},
];

//Paso1: Convertimos en Arrowfuntion el forEach
//Si solo tienes un parametro, puedes eliminar los parentesis del parametro
//De la misma manera, si solo hay una instruccion en el cuerpo de la funcion puede eliminar las llaves

let resultado;
meses.forEach(mes=>console.log(mes));
console.log(resultado);

//Paso2: Covierte el en ArrowFunction lo siguiente
meses.forEach(mes=>{
    if (mes=='Marzo'){
        console.log('Marzo si existe');
    }
});

//Si tenemos un return en una funcion, al convertirlo en arrow Function si solo tiene una linea de retorno, el return se omite, al igual que las llaves de cuerpo
//de la funcion
let resultado3=carrito.some(producto=> producto.nombre==='Celular');
console.log(resultado3);

//Recuerda que en esta funcion tienes 2 parametro en la funcion, NO SE OMITEN los parentesis
resultado=carrito.reduce((total, producto)=>resultado + producto.precio,0);
console.log(resultado);

resultado=carrito.filter(producto=> producto.precio>800);
console.table(resultado);

resultado=carrito.filter(producto=>producto.nombre=='Celular');
console.table(resultado);

resultado=carrito.filter(producto=>producto.nombre!=='Celular');
console.table(resultado);

//Si comparas el codigo podras notar que habra menos codigo
// ya que su sintaxis es mas corta
```

## Método Foreach y Método Map
### Foreach
forEach en JavaScript es un método de los arrays que ejecuta una función para cada elemento del arreglo. Es una forma de iterar que no requiere un contador manual como un bucle for tradicional. En lugar de eso, llama a una función de callback una vez por cada elemento, pasando el elemento actual a esa función. 

### Ejercicio 18.js:
Procedimiento:
- Crea un archivo llamado 18.js
- Enlaza tu archivo .js externo al html

```javascript
const carrito=[
    {nombre:'Monitor 20 Pulgadas', precio:500},
    {nombre:'Television 50 pulgadas', precio:8000},
    {nombre:'Tableta 9 Pulgadas', precio:5000},
    {nombre:'Celular', precio:7000},
    {nombre:'Bocinas', precio:500},
    {nombre:'Laptop', precio:21000},
];

//ForEach

carrito.forEach(function(producto){
    console.log(producto.nombre)
});
```

### Método Map
El método map() en JavaScript crea un nuevo array aplicando una función a cada elemento de un array existente, devolviendo un nuevo array con los resultados sin modificar el original. Es una forma útil de transformar los elementos de un array, como por ejemplo, elevarlos al cuadrado, formatear texto o filtrar objetos. 

- Agrega el siguiente código al mismo ejercicio llamado 17.js
- Guarda cambios y visualiza en la consola del navegador
```javascript
const arreglo=carrito.map(function(producto){
    return producto.nombre
});
console.log(arreglo);
```
Aplicando Arrow Function, los métodos ForEach y Map quedarían de la siguiente manera:
```javascript
//ForEach
carrito.forEach(producto=>console.log(producto.nombre));

//Map
const arreglo=carrito.map(producto=> producto.nombre);
console.log(arreglo);
```

##  This en JavaScript
En JavaScript, this es una palabra clave que hace referencia al contexto de ejecución de una función. Su valor cambia según la forma en que se llama a la función, por lo que puede referirse al objeto que contiene el método, al objeto global (window en el navegador), a una instancia nueva, o a un objeto enlazado explícitamente. 

### Ejercicio 19.js:
Procedimiento:
- Crea un archivo llamado 19.js
- Enlaza tu archivo .js externo al html

  En el ejercicio:
- Creamos un objeto llamado reservacion
- Tendra 4 propiedades (nombre, apellido, total y pagado)
- y 1 funcion llamada informacion()

```javascript
const reservacion={
    nombre:'Naty',
    apellido: 'Juarez',
    total: 5000,
    pagado: false,
    informacion: function(){
        console.log(`El cliente ${this.nombre} reservo y su cantidad a pagar es de ${this.total}`);
    }
}

//invocamos la funcion informacion del objeto reservacion
reservacion.informacion();
```
 Cuando se llama a una función como método de un objeto, `this` se vincula a ese objeto. Por ejemplo en:
  ```javascript
  console.log(`El cliente ${this.nombre} reservo y su cantidad a pagar es de ${this.total}`);
```
 - this.nombre: vincula la propiedad nombre con el objeto en el que se encuentra definida la función, es decir **reservacion**

 Agrega el siguiente código al mismo ejercicio, observa que aunque el nombre de las propiedades del objeto sean iguales, con This se hace referencia a que se mmostrará las propiedad nombre y total del objeto **reservacion2**.
 ```javascript
const reservacion2={
    nombre:'Angelica',
    apellido: 'Rodriguez',
    total: 8000,
    pagado: false,
    informacion: function(){
        console.log(`El cliente ${this.nombre} reservo y su cantidad a pagar es de ${this.total}`);
    }
}
reservacion2.informacion();
```
## Object Literal y Object Constructor

### Object Literal
Un objeto literal en JavaScript es una forma concisa de crear y definir un objeto directamente en una variable, utilizando llaves {} para agrupar pares clave-valor. Es útil para crear objetos simples sobre la marcha y permite asignar propiedades (datos) y métodos (funciones) de manera directa.

**Características principales**

- Sintaxis simple: Se define el objeto dentro de llaves {}.
- Pares clave-valor: Contiene propiedades que son pares de clave (un identificador) y valor (el dato).
- Tipos de valores: Los valores pueden ser de cualquier tipo de dato, como strings, números, booleanos, arrays o incluso otros objetos.
- Métodos: Se pueden incluir funciones como métodos directamente dentro del objeto. La sintaxis moderna (desde ES6) permite omitir la palabra clave function y los dos puntos para declarar métodos de forma más limpia.
- Flexibilidad: Permite añadir o modificar propiedades y métodos después de su creación. 

Nota: En JavaScript, los literales son valores fijos que se escriben directamente en el código.

### Ejercicio 20.js:
Procedimiento:
- Crea un archivo llamado 20.js
- Enlaza tu archivo .js externo al html

**Ejemplo de uso:**
```javascript
//Object Literal
//Creacion del objeto miproducto
const miproducto={
    nombre:'Tablet',
    precio: 500
}
//Creacion del objeto miproducto2
const miproducto2={
    nombre:'Tablet',
    precio: 500
}
//Creacion del objeto miproducto3
const miproducto3={
    nombre:'Tablet',
    precio: 500
}
console.log(miproducto);
console.log(miproducto2);
console.log(miproducto3);
```
### Object Constructor
Un constructor en JavaScript es una función especial que se usa para crear e inicializar objetos. Se invoca automáticamente cuando se crea una nueva instancia de un objeto usando la palabra clave new. Su propósito es definir las propiedades y establecer los valores iniciales de un objeto de forma reutilizable. 

**Características clave**
- Función especial: Se utiliza para "construir" o crear nuevas instancias de un tipo de objeto.
- Palabra clave new: El constructor se llama usando new, lo que crea un nuevo objeto y devuelve una instancia de ese objeto.
- Inicialización: Asigna valores a las propiedades del objeto en el momento de su creación.
- Reutilización de código: Permite crear múltiples objetos con la misma estructura y propiedades sin tener que escribir el mismo código repetidamente.
- this: Dentro del constructor, this se refiere a la nueva instancia del objeto que se está creando. Se utiliza para asignar propiedades al objeto, como this.nombre = nombre.

  **Agrega el siguiente codigo al ejercicio 20:**
```javascript
//Object Constructor
function Producto(nombre,precio){
    this.nombre=nombre;
    this.precio=precio;
}

//Creacion de objetos usando el constructor Producto
const producto2= new Producto('Monitor de 50"', 800);
const producto3=new Producto('Laptop', 3000);
const producto4=new Producto('Mouse inalambrico', 350);

console.log(producto2);
console.log(producto3);
console.log(producto4);
```
  
