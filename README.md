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
	
  ```assembly
.data
    n1: .asciiz "enter your first number: "
    n2: .asciiz "enter your second number: "
    result: .asciiz "result is "
.text
    #getting first input.
    la $a0, n1
    li $v0, 4
    syscall
    li $v0, 5
    syscall
    move $t0, $v0
    #getting second input.
    la $a0, n2
    li $v0, 4
    syscall
    li $v0, 5
    syscall
    move $t1, $v0
    #calculate and print out the result.
    la $a0, result
    li $v0, 4
    syscall
    add $t3, $t0, $t1
    move $a0, $t3
    li $v0, 1
    syscall
    #end program.
    li $v0, 10
    syscall
              
              
      .data
	      message: .asciiz "\nHello what your name? "
	      message2: .asciiz "\n Nice to meet you "
	      userImput: .space 20
  .text
	      main:
              li $v0, 4
              la $a0 message
              syscall
	      # Getting user's input as text
	      li $v0, 8
              la $a0, userImput
              li $a1, 20
              syscall
              #Display Nice to meet you
              li $v0, 4
              la $a0 message2
              syscall
              #Display the name
              li $v0, 4
              la $a0 userImput
              syscall
              li $v0, 10
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
		   
		   
		   
# Week challenges (Monday) 
		   
Read about: if...else

The if statement executes a statement if a specified condition is truthy
Syntax
if (condition)
  statement1

// With an else clause
if (condition)
  statement1
else
  statement2		   
		   
Read about: for
		   
The for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by a statement (usually a block statement) to be executed in the loop.															
Syntax
for ([initialization]; [condition]; [final-expression])
  statement		   
let str = '';

for (let i = 0; i < 9; i++) {
  str = str + i;
}

console.log(str);
// expected output: "012345678"
	
initialization
An expression (including assignment expressions) or variable declaration evaluated once before the loop begins. Typically used to initialize a counter variable. This expression may optionally declare new variables with var or let keywords

condition
An expression to be evaluated before each loop iteration. If this expression evaluates to true, statement is executed. If the expression evaluates to false
	
statement
A statement that is executed as long as the condition evaluates to true. To execute multiple statements within the loop, use a block statement ({ /* ... */ }) to group those statements.
	

Read about: while
	
The while statement creates a loop that executes a specified statement as long as the test condition evaluates to true. The condition is evaluated before executing the statement.

Try it
	
		   
let n = 0;

while (n < 3) {
  n++;
}

console.log(n);
// expected output: 3		   
		   	
Syntax
	     
while (condition)
  statement
	     
condition
An expression evaluated before each pass through the loop. If this condition evaluates to true, statement is executed. When condition evaluates to false, execution continues with the statement after the while loop.
	     
statement
An optional statement that is executed as long as the condition evaluates to true. To execute multiple statements within the loop, use a block statement ({ /* ... */ }) to group those statements.	     
	     
	     
	     
	     
		   
		   
		   
		   
