# Test de Javascript

Esta es una prueba que es parte del curso practico de Javascript dentro de la plataforma Platzi. Para resolver estas preguntas, lo haré en primera instancia con mis propias palabras y posteriormente complementar algunos conceptos que hagan falta con ayuda de Internet y IA.

------------

1.  [Variables y operaciones](###variables-y-operaciones)
2. [Funciones](###funciones)
3. [Condicionales](###condicionales)
4. [Ciclos](###ciclos)
5. [LIstas](###listas)

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
Una funcion permite realizar** una o multiples operaciones** en un bloque de codigo de programacion. Es decir, es la manera de usar una serie de instrucciones para modificar un valor y obtener un resultado dadas ciertas condiciones.

- ¿Cuándo me sirve usar una función en mi código?
 Las funciones pueden **ahorrar tiempo**, pues ayudan a realizar operaciones repetitivas, entonces, sirve usar una uncion cuando quiero reutilizar codigo multiples veces. Ademas no necesariamente deben devolver un resultado, pero si deben realizar una o muchas operaciones para un fin.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
Es una nocion similar a la de declarar una variable e iniciar una variable.

	Los parametros en una funcion es la manera de definir que **valores espera recibir una funcion ** en su sintaxis. 
	e.g: 
	function ejemplo(**parametro1, parametro2,...**){}

	Los argumentos en una funcion son los valores que toman dichos parametros una vez la funcion ha sido llamada.
	e.g:
	ejemplo(**argumento1, argumento2...**)
	function ejemplo(parametro1, parametro2,...){}

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
Existen 3 tipos de condicionales en Javascript. 
	 - If - else: 
	 	Este condicional ejecuta una sentencia de verdad para evaluar si se cumple una condicion. En caso de que se cumpla, ejecuta el primer bloque de codigo encerrado por corchetes **if {}** , en caso de que no se cumpla, se ejecuta el segundo bloque de codido encerrado por los corchetes. **else {}**
		```
		if ( a > b){
		primer bloque de codigo...
		} else {
		segundo bloque de codigo...
		}
		```
	 - if - else -if: 
	 	Es muy similar al condicional if - else con el adicional de que se anidan multiples bloques de codigo donde se añaden nuevas condiciones.
		```
		if ( a > b){
		primer bloque de codigo...
		} else if ( b > c ){
		segundo bloque de codigo...
		} else if ( c > d ){
		tercer bloque de codigo...
		}else{
		bloque final de codigo
		}
		```
	 - switch:
	  Realiza multples evaluaciones de una variable y segun su resultado, rejecuta el bloque de codigo correspondiente.
	  ```
	  switch (expresion) {
  		case valor1:
    		// Bloque de código a ejecutar si la expresion es igual a valor1
    		break;
  		case valor2:
    		// Bloque de código a ejecutar si la expresion es igual a valor2
    		break;
  		// Más casos...
  		default:
    		// Bloque de código a ejecutar si ninguno de los casos anteriores coincide
}
	  ```

- ¿Puedo combinar funciones y condicionales?
Si, se pueden combinar y de hecho son muy necesarias para poder realizar las tareas de una funcion.A modo de ejemplo, puedo recibir en la funcion un digito a evaluar dentro de un condicional para saber si es un numero par o no:
```
	esPar(2);
	
	function esPar( numero ){
	
		if( numero % 2 == 0){
			console.log('El numero es Par');
			return true;
	} else {
			console.log('El numero es Impar');
			return false;
	}
```

2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
```
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
```
Solucion
```
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion == 'Free') {
       console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion ==  "Basic"){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion ==  "Expert"){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else {
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏
```
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion == 'Free') {
       console.log("Solo puedes tomar los cursos gratis");
}

if (tipoDeSuscripcion ==  "Basic"){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}

if (tipoDeSuscripcion ==  "Expert"){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} 

if (tipoDeSuscripcion ==  "ExpertPlus"){
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```
Reto
```
const tipoDeSuscripcion = "Basic";

const mensajesSuscripcion = {
  Free: "Solo puedes tomar los cursos gratis",
  Basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
  Expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
  ExpertPlus: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
};

console.log(mensajesSuscripcion[tipoDeSuscripcion] || "Tipo de suscripción no reconocido");
```
------------

### Ciclos
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es un ciclo?
Un ciclo permite realizar la misma operacion una n cantidad de veces con un incremento determinado o hasta que se cumpla una condicion.
- ¿Qué tipos de ciclos existen en JavaScript?
Existen 4 tipos de ciclo:
	- For: Se compone de una inicialización, una condición de continuación y una expresión de incremento. 
```
for (let i = 0; i < 5; i++) {
  // Bloque de código a ejecutar en cada iteración
}
```
	- While:  se utiliza para ejecutar un bloque de código mientras se cumple una condición determinada. La condición se verifica antes de cada iteración, y si es verdadera, el bloque de código se ejecuta.
	```
	while (condicion) {
  // Bloque de código a ejecutar mientras la condición sea verdadera
}
	```

	-  Do - While:  es similar al ciclo while, pero la diferencia radica en que la condición se verifica después de ejecutar el bloque de código. Esto garantiza que el bloque de código se ejecute al menos una vez, incluso si la condición inicialmente es falsa.
```
do {
  // Bloque de código a ejecutar al menos una vez
} while (condicion);
```
	- For - in:  se utiliza para iterar sobre las propiedades de un objeto. Recorre todas las propiedades enumerables del objeto y ejecuta el bloque de código para cada propiedad.
```
for (let key in objeto) {
  // Bloque de código a ejecutar para cada propiedad
}
```
- ¿Qué es un ciclo infinito y por qué es un problema?
Como su nombre lo indica, un ciclo infinito se ejecuta sin fin o **sin una condicion que haga que termine su ejecucion. **Puede ser un problema, ya que cada ejecucion dentro de este ciclo ocupa espacio en memoria y capacidad de procesamiento de la maquina donde se ejecuta, ademas pueden causar que el programa se **bloquee o se vuelva irresponsivo**, lo que puede llevar a un **mal funcionamiento del programa** o incluso al bloqueo completo del sistema. Dando lugar a un agotamiento de los recursos y afectar el** rendimiento general del sistema**, como cuellos de botella, problemas de procesamiento y hasta de capacidad de almacenamiento. 

- ¿Puedo mezclar ciclos y condicionales?

Si se pueden mezclar y de hecho se complementan, pues lo que realiza un ciclo es una ejecucion repetitiva de codigo y el condicional evaluaria una sentencia de verdad para este codigo, lo que ayudaria en ciertos escenarios a descartar valores dentro de un arreglo o objeto.

2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:
```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}
```
Solucion:
```
let i = 0
do{
	    console.log("El valor de i es: " + i);
		 i++;
}while(i < 5);
```

2 ciclo:
```
for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```
Solucion:
```
let i = 10
do{
	    console.log("El valor de i es: " + i);
		 i--;
}while(i >= 2);
```
3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.
```
do{
let valor = prompt("¿Cuanto es 2 + 2 ? ")
if()
}while()
```

------------

### Listas
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es un array?
Un array es la manera de almacenar **multiples valores dentro de una sola variable** para que puedan ser accedidos de una manera **indexada**. Es decir, que cada elemento dentro del array tiene un indice que lo identifica, ademas de que pueden ser elementos de **diferente tipo.** Cada elemento se separa del otro por una coma. Tienen la particularidad de que la indexacion empieza desde 0, por lo que el primer elemento del array, se encuentra en el indice 0.
```
let array = [ 1, 2, '3', 'Sabroso', boolean, '03-04-23'] ;
array[3] // 'Sabroso'
```

- ¿Qué es un objeto?
Un objeto es similar a un array debido a que en el tambien se almacenan multiples valores, con la diferencia de que la manera en que se acceden a estos valores es con una **llave**. El objeto se carateriza por tener una estructura **llave:valor**, donde la llave es la manera de identificar un atributo del objeto y el valor contiene el dato almacenado. Para acceder al conjunto llave:valor del objeto se realiza **colocando un punto .** despues del nombre de la variable objeto. Incluso pueden almacenar **funciones** que pueden ser llamadas al acceder al objeto.

```
const persona = {
  nombre: "Juan",
  edad: 30,
  esEstudiante: true,
  intereses: ["programación", "música", "deportes"],
  direccion: {
    calle: "Calle Principal",
    ciudad: "Ciudad Principal",
    pais: "País Principal"
  },
 function saludar() {
    console.log("¡Hola! Mi nombre es " + this.nombre);
  }
};

console.log(persona.nombre); // "Juan"
console.log(persona.edad); // 30
console.log(persona.intereses[0]); // "programación"
console.log(persona.direccion.ciudad); // "Ciudad Principal"
persona.saludar(); // Imprime "¡Hola! Mi nombre es Juan"
```
- ¿Cuándo es mejor usar objetos o arrays?
Cuando la situacion requiera crear **multiples instancias con una estructura similar** conviene utilizar **objetos** pues estos pueden comportarse de diferentes maneras y ademas almacenar **funciones**, ademas permiten acceso a los datos de manera personalizada con el uso de **llaves con nombre**. Cuando simplemente se requiera almacenar** multiples elementos de manera secuencial** y  sin importar su valor, es mejor utilizar un array, pues unicamente es necesario conocer el **indice** del valor. 
En general, si los datos se pueden organizar de manera más natural utilizando claves descriptivas y se necesita una estructura más compleja, los objetos son una elección adecuada. Por otro lado, si se trata de una lista ordenada de datos o se requieren operaciones comunes como agregar, eliminar y buscar elementos, los arrays son más apropiados.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
SI, se pueden mezclar objetos que contengan arrays y viceversa, de hecho, los arrays en JavaScript también son objetos.

2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```
let clubes = ['FC Barcelona','Manchester United','Juventus FC'];

primerElemento(clubes);
function primerElemento(array){
	console.log('El primer elemento es:' +array[0]);
}
```

3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
```
let clubes = ['FC Barcelona','Manchester United','Juventus FC'];

todos(clubes);
function todos(array){
	for(let i=0; i < array.length; i++){
	console.log('El  elemento '+ i +' es:' +array[i]);
	}
}
```
4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
```
let clubes = {
  equipo1: 'FC Barcelona',
  equipo2: 'Manchester United',
  equipo3: 'Juventus FC'
};

todos(clubes);

function todos(objeto) {
  for (let club in objeto) {
    console.log(objeto[club]);
  }
}
```
