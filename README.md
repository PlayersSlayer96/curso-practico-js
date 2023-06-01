# curso-practico-js

# Test de Javascript

Esta es una prueba que es parte del curso practico de Javascript dentro de la plataforma Platzi. Para resolver estas preguntas, lo haré en primera instancia con mis propias palabras y posteriormente complementar algunos conceptos que hagan falta con ayuda de Internet y IA.

------------

1.  [Variables y operaciones](####variables-y-operaciones)
2. [Funciones](####funciones)
3. [Condicionales](####condicionales)

------------

### Variables y operaciones 

1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?
Una variable es la manera de almacenar un valor en memoria que no es constante, es decir que puede ser modificado a lo largo del tiempo y dependiendo de la necesidad del software. Sirve (asi como en las matematicas) para aplicar valores independientes a una formula, operacion o **funcion** y obtener un resultado a partir de este o modificar un comportamiento especifico.

- ¿Cuál es la diferencia entre declarar e inicializar una variable?
Declarar una variable permite determinar esta variable que **nombre y que tipo tendra**, mientras que inicializar una variable es **establecer un valor inicial **para poder ser utilizada posteriormente dentro de un programa.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
Numeros y strings son dos tipos de datos diferentes, por tanto, producen resultados diferentes al aplicarles un operador '+' entre si.
Sumar **numeros** es una operacion aritmetica. e.g. 2 + 2 = 4.
Concatenar **strings** es una operacion 'no aritmetica' y no suma digitos sino encadena caracteres o cadenas de texto. e.g. '2' + '2' = '22'

- ¿Cuál operador me permite sumar o concatenar?
Como dicho en el punto anterior, el operador que permite sumar (numeros o *int*) y concatenar (cadenas o *strings*) es el operador **+**

2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:
Nombre = 'string'
Apellido = 'string'
Nombre de usuario en Platzi = 'string'
Edad = int
Correo electrónico = 'string'
Mayor de edad = boolean
Dinero ahorrado = float
Deudas = float
3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
```
var nombre = 'Armando'; //string
var apellido = 'Barreda'; //string
var nombreUsuarioEnPlatzi = 'cosme_Fulanito_20'; //string
var edad = 25; // int
var correoElectronico = 'pepito@perez.com';// string
var mayorDeEdad = true; // boolean
var dineroAhorrado = 1000.50; // float
var deudas = 500.75; // float
```
4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
```
//Nombre completo (nombre y apellido)
console.log(nombre + " " +apellido)
//Dinero real (dinero ahorrado menos deudas)
console.log()
//Funciones
function calcularDineroReal(dineroAhorrado, deudas){
	return dineroAhorrado - deudas
}
```
------------
### Funciones

1️⃣ Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es una función?
Una funcion permite realizar **una o multiples operaciones** en un bloque de codigo de programacion. Es decir, es la manera de usar una serie de instrucciones para modificar un valor y obtener un resultado dadas ciertas condiciones.

- ¿Cuándo me sirve usar una función en mi código?
 Las funciones pueden **ahorrar tiempo**, pues ayudan a realizar operaciones repetitivas, entonces, sirve usar una uncion cuando quiero reutilizar codigo multiples veces. Ademas no necesariamente deben devolver un resultado, pero si deben realizar una o muchas operaciones para un fin.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
Es una nocion similar a la de declarar una variable e iniciar una variable.

	Los parametros en una funcion es la manera de definir que **valores espera recibir una funcion** en su sintaxis. 
	e.g:
	```
	function ejemplo(**parametro1, parametro2,...**){}
	```
	Los argumentos en una funcion son los **valores que toman dichos parametros** una vez la funcion ha sido llamada.
	e.g:
	```
	ejemplo(**argumento1, argumento2...**)
	function ejemplo(parametro1, parametro2,...){}
	```

2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:
```
const name = "Juan David";
const lastname = "Castro Gallego";
const nickname = "juandc";

nickName(name, lastname,nickname);

function nickName(name1, name2, nickname){
const completeName = name1 + name2;
console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
}
```

------------

### Condicionales
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es un condicional?
Un condicional es una operacion en la cual se evalua una verdad segun una sentencia, principalmente de **comparacion** entre dos valores o para determinar **si se cumple una condicion o no.**
e.g:
```
if( a > b){}
if( nombre === 'BETO')
```

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
Existen 3 tipos de condicionales en 

- ¿Puedo combinar funciones y condicionales?
2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

Ciclos
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
¿Qué es un ciclo?
¿Qué tipos de ciclos existen en JavaScript?
¿Qué es un ciclo infinito y por qué es un problema?
¿Puedo mezclar ciclos y condicionales?
2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.

Listas
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
¿Qué es un array?
¿Qué es un objeto?
¿Cuándo es mejor usar objetos o arrays?
¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
