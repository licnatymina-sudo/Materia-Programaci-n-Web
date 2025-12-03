# Programación en Java Script
## Funciones
Las funciones en JavaScript son bloques de código reutilizables que realizan tareas específicas. Se definen con la palabra clave function, un nombre, parámetros entre paréntesis y un conjunto de instrucciones entre llaves. Para que se ejecuten, deben ser "llamadas" por su nombre. Permiten encapsular lógica, organizar el código y evitar la repetición. 
### Componentes principales
- Palabra clave function: Indica que se está definiendo una función.
- Nombre de la función: Un identificador para llamar a la función. Es opcional en funciones anónimas.
- Paréntesis (): Contienen los parámetros (variables internas) que la función puede recibir.
- Llaves {}: Encierran el código que se ejecutará al llamar a la función.

## /*Uso de Funciones*/
/*Creación de una función con parametro y argumentos*/

function sumar(numero1, numero2){
    console.log(numero1+numero2);
}

sumar(10,5); //invocación del metodo con argumentos
sumar(3,3);
sumar(200,300);

/*Expresión de una función*/
const sumar2= function(n1,n2){
    console.log(n1+n2);
}
sumar2(7,560);  /*Invocacionn del metodo sumar*/

