# Week challenges (Monday) 💻
1. [x] Watch Object Oriented Programming - The Four Pillars of OOP

Surrounds the topics of
* Abstraction: Show the user only the necessary details
* Inheritance: code reusability
* Polymorphism: Determina which functions to run while the programm is running
* Encapsulation: setting to private certain properties to still encapsulate within the object

3. [x] Readme - OOP exercise

Definitons of the main concepts:

* Class: Set of instructions.
* Object: File that contains the properties or characteristics.
* Instance: When data is assigned and called along the object.
* Interface: Is the variables and data that holds within the blocks. Lives in the memory. You don't have to have a class created.
* Access Modifiers: It's where we can get and set more that to the values stablished already.
* Constructors: is where we define the parameters for values for the instance or static properties.
* Methods: are behaviours or actions.

### Example
This is my guide to show an example on how to use OOP in typescript:
#### Object
![image](https://user-images.githubusercontent.com/98929413/187808072-0de48f03-732c-4454-a46c-6b06a235e759.png)

For this case, I'm creating an object class for movies. Movies can have a genre, a year of creation and whether or not they have a prequel or sequel. 

#### Encapsulation
![image](https://user-images.githubusercontent.com/98929413/187809024-d5709d05-3b96-49f4-8d20-91215ff7352a.png)


#### Accessors
![image](https://user-images.githubusercontent.com/98929413/187815594-c6c48ffe-9b31-4b03-9468-5466bd0d2e6e.png)


#### Instances
![image](https://user-images.githubusercontent.com/98929413/187813829-6da0e2a6-f6b2-4afe-9fe0-3853208a5a9c.png)


#### Interfaces
![image](https://user-images.githubusercontent.com/98929413/187811010-80d369c2-37d0-42d8-ae6e-2c73e7a7a49b.png)



### Class: is the overall picture for all the previous sections created

# Week challenges (Tuesday) 💻
3. [x] Input/Output playground, using Typescript

Just a screenshot from the things I found the most interesting while doing this exercise:
![image](https://user-images.githubusercontent.com/98929413/187842590-82f470ce-ead9-43c2-9e80-15ca0972b574.png)

![image](https://user-images.githubusercontent.com/98929413/188008269-c02967a0-b884-48d7-a270-e73146b65880.png)

# Week challenges (Wednesday) 💻
4. [x] Build Tower exercise, using Typescript
```Typescript
export const towerBuilder = (nFloors: number): string[] => {
  // build here ["  *  ", "  ***  ", "  *****  "] => ["  *  ", "  ***  ", "  *****  ", "  *******  ", "  *********  "]
  //We know that if nFloors === 1 returns ['*'];
  if(nFloors === 1) return ['*'];
  //1. Put a var to return the new array
  let result: string[] = [];
  //2. We expand the number array with iteration
  for (let i = 1; i <= nFloors; i++) {
    //3. We push for the new array with literal templates
    //considering the fact that the formula is to multiply by two and substract one (2n-1) ==> (n*2) - 1
    result.push(`${' '.repeat(nFloors - i)}${'*'.repeat(2 * i - 1)}${' '.repeat(nFloors - i)}`);
  }
  //4. We return the result
  return result;
}
```
6. [x] Meeting exercise, using Typescript
```Typescript
export function meeting(s: string): string {
  return s
  //1. Pasar el string to uppercase
  .toUpperCase()
  //2. Se corta todo el string, dentro un arreglo como una sola unidad grande 
    .split(';')
  //3. como ya está en tipo arreglo pero como unidad grande, procedemos a crear un nuevo arreglo con .map()
  //donde podemos decir que, en redacción con signo + '(' + los puntos : se convierten a coma con (':')
  //con el .reverse() es como le decimos que comience por el apellido y después nombre
  //luego, con un (', ') le decimos que nos agregue la coma entre el apellido ya en primer lugar, y seguido del nombre
  //cerramos paréntesis con + ')'
    .map((n: string) => '(' + n.split(':').reverse().join(', ') + ')' )
  //ordenamos por oden alfabetico
    .sort()
  //lo regresamos a un arreglo donde fuera de los paréntesis no tienen coma, sigue siendo una unidad grande dentro del array
    .join('');
}
```

# Week challenges (Thursday) 💻
6. [x] Interfaces guided exercise, using Typescript
```Typescript
//About using TypeScript interfaces
interface IceCream {
  flavor: string;
  scoops: number;
  instructions?: string;
}

let myIceCream: Sundae = {
  flavor: 'vanilla',
  scoops: 2,
  sauce: 'caramel',
  nuts: true
}
console.log(myIceCream.flavor);

function tooManyScoops(dessert: Sundae) {
  if (dessert.scoops >= 4) {
    return dessert.scoops + ' is too many scoops!';
  } else {
    return 'Your order will be ready soon!';
  }
}

console.log(tooManyScoops({flavor: 'vanilla', scoops: 5, sauce: 'caramel'}));
//extend the interface
interface Sundae extends IceCream {
  sauce: 'chocolate' | 'caramel' | 'strawberry';
  nuts?: boolean;
  whippedCream?: boolean;
  instructions?: string;
}
```
Declaring and implementing interfaces
```Typescript
/* Module 3: Implement interfaces in TypeScript
   Lab Start  */

/*  EXERCISE 1
    TODO: Declare the Loan interface. */
interface Loan {
    principal: number,
    interestRate: number
}

/*  TODO: Declare the ConventionalLoan interface. */
interface ConventionalLoan extends Loan {
    months: number
}


/*  TODO: Update the calculateInterestOnlyLoanPayment function. */
function calculateInterestOnlyLoanPayment(loanTerms: Loan): string {
    let interest = loanTerms.interestRate / 1200;
    let payment;
    payment = loanTerms.principal * interest;
    return 'The interest only loan payment is ' + payment.toFixed(2);
}

let interestOnlyPayment = calculateInterestOnlyLoanPayment({ principal: 30000, interestRate: 5 });
console.log(interestOnlyPayment);

/*  TODO: Update the calculateConventionalLoanPayment function. */

function calculateConventionalLoanPayment(loanTerms: ConventionalLoan): string {
    // Calculates the monthly payment of a conventional loan
    let interest: number = loanTerms.interestRate / 1200; // Calculates the Monthly Interest Rate of the loan
    let payment: number;
    payment = loanTerms.principal * interest / (1 - (Math.pow(1 / (1 + interest), loanTerms.months)));
    return 'The conventional loan payment is ' + payment.toFixed(2);
}

let conventionalPayment = calculateConventionalLoanPayment({ principal: 30000, interestRate: 5, months: 180 });
console.log(conventionalPayment)

//let interestOnlyPayment = calculateInterestOnlyLoanPayment(30000, 5);
//let conventionalPayment = calculateConventionalLoanPayment(30000, 5, 180);

//console.log(interestOnlyPayment);     //* Returns "The interest only loan payment is 125.00" 
//console.log(conventionalPayment);     //* Returns "The conventional loan payment is 237.24" 
```

