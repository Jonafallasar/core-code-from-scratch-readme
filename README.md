# Tareas primera semana
# Martes 19 de julio, 2020
1. create an explanation aboutInterpreted And Compiled Programming Languages

# Cada programa es un conjunto de instrucciones, ya sea para agregar dos números o enviar una solicitud a través de internet.
1.Idiomas compilados
Los lenguajes compilados se convierten directamente en código de máquina que el procesador puede ejecutar . Como resultado, tienden a ser más rápidos y eficientes de ejecutar que los lenguajes interpretados. También le dan al desarrollador más control sobre los aspectos del hardware, como la administración de la memoria y el uso de la CPU.
Ejemplos de lenguajes compilados puros son C, C++, Erlang, Haskell, Rust y Go.

Idiomas interpretados
Los intérpretes ejecutan un programa línea por línea y ejecutan cada comando.
Ejemplos de lenguajes interpretados comunes son PHP, Ruby, Python y JavaScript.

2. Is Java compiled or interpreted, or both?, check the sources and answer the question in your README
Es un hibrido  por lo que es posible ser ejecutado por un hardware CPU.un programa Java primero se compila en un código de bytes que JRE puede entender. ByteCode luego es interpretado por la JVM convirtiéndolo en un lenguaje interpretado.


3.Ejercicio de conversión de moneda de pseudocódigo
1.  Starting point: START
  Input: READ, GET, GET FROM(<URL>)
  Output: PRINT
  Math: +, -, *, /
  Assignation: <--
  Initialize: SET, INIT
  Add one: INCREMENT
  End point: END
  
    1. START
  2. Amount <-- GET
  3. BTCprice <-- GET FROM(https://www.coindesk.com/price/bitcoin/)
  4. Total <-- Amount * BTCprice
  5. PRINT Total
  
  
  4. Aprende sobre lenguajes de alto y bajo nivel
  Lenguaje de bajo nivel
  Es un lenguaje de programación que proporciona poca  o ninguna abstracción de los conceptos de programación y esta muy cerca del hardware .
  Tiene un control completo sobre cosas como la asignación de memoria, lo que los  hace muy eficientes por eso son excelentes para escribir sistemas operativos o firmware.
  
  Lenguaje de alto nivel
  Estan más cerca del lenguaje humano y debido a que tienen  abstracciones  muy solidas, es más fácil de leer, escibir  y mantener. Los programadores no tienen que pensar en cosas como registros  o administración de memoria.
  El desarrollo de un programa es más simple.
  
  # Week challenges (Wednesday)
  1-Your date of birth in the matrix? exercise
  
  00000011111
  
  1.Create a program that adds any two given numbers provided by the user
  2.Create a program that displays your name
  
       .data
        welcome: .asciiz "\n================= Welcome =================\n"
        result: .asciiz "\nThe result is: "
        number_one_msg: .asciiz "\nEnter the first number: "
        number_two_msg: .asciiz "\nEnter the second number: "
  .text
        main:
              # welcome message
              li $v0, 4
              la $a0, welcome
              syscall

              # user input
              li $v0, 4
              la $a0, number_one_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t0, $v0

              # user input
              li $v0, 4
              la $a0, number_two_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t1, $v0

              # adding the user numbers
              add $t2, $t0, $t1

              # showing result number
              li $v0, 4
              la $a0, result
              syscall

              # printing number
              li $v0, 1
              move $a0, $t2
              syscall
              
              
      .data
	      my_name: .asciiz "\nJona\n"
  .text
	      main:
              li $v0, 4
              la $a0, my_name
              syscall
              
  
  
  
  
  
Week challenges (Thursday)
  
  In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise
  
  For
While
do While
Even number
Reminder Operator

For
for (var i = 0; i <= 100; i++) {
  if (i % 2 == 0) console.log(i);
}

While
var i = 0;
while (i <= 100) {
  if (i % 2 == 0) console.log(i);
  i++;
}

do While
var i = 0;
do {
  if(i % 2 == 0)console.log(i);
  i++
} w
  
  Bad code
  
  var cond = false;

if (cond) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}

Bad code 2

var n = 100;

if (n == 100) {
  console.log('This is a special number!');
} else if (n < 1000 && n % 10 == 0) {
  console.log('This number is almost special');
} else {
  console.log('Just a regular number');
  }
  9. END
