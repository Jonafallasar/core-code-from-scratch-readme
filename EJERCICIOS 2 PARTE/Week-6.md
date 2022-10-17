# Monday 22 august, 2022
1. [x] Declare variable types in TypeScript guided exercise, using Typescript
```Typescript
/*  EXERCISE 1
    TODO: Modify the code to add types to the variable declarations. 
    The resulting JavaScript should look the same as the original example when you're done. */

let firstName: string;
let lastName: string;
let fullName: string;
let age: number;
let ukCitizen: boolean;

firstName = 'Rebecca';
lastName = 'Smith';
age = 42;
ukCitizen = false;
fullName = firstname + " " + lastname;

if (ukCitizen) {
    console.log("My name is " + fullName + ", I'm " + age + ", and I'm a citizen of the United Kingdom.");  
} else {
    console.log("My name is " + fullName + ", I'm " + age + ", and I'm not a citizen of the United Kingdom.");
}

/* EXERCISE 2
   TODO: You can use types to ensure operation outcomes. Run the code as is and then modify 
   it to have strongly typed variables. Then, address any errors you find so that the result 
   returned to a is 12. */

let x: number;
let y;
let a;

x = 5;
y = 7;
a = x + y;

console.log(a);

/* EXERCISE 3
   TODO: In the following code, implement an enum type called Season that represents 
   the constants "Fall", "Winter", "Spring", and "Summer". Then, update the function so 
   you can pass in the season by referencing an item in the enum, for example 
   Season.Fall, instead of the literal string "Fall". */

enum Season {
    Winter,
    Spring,
    Summer,
    Fall
};

function whichMonths(season: Season) {

    let monthsInSeason: string;

    switch (season) {
        case Season.Fall:
            monthsInSeason = "September to November";
            break;
        case Season.Winter:
            monthsInSeason = "December to February";
            break;
        case Season.Spring:
            monthsInSeason = "March to May";
            break;
        case Season.Summer:
            monthsInSeason = "June to August";
    }

    return monthsInSeason;
}

console.log(whichMonths(Season.Fall));

/* EXERCISE 4
   TODO: Declare the array as the type to match the type of the items in the array. */

   let randomNumbers: number[] = [];
   let nextNumber: number;
   
   for (let i = 0; i < 10; i++) {
       nextNumber = Math.floor(Math.random() * (100 - 1)) + 1;
       randomNumbers.push(nextNumber);
   }
   
   console.log(randomNumbers);
```
3. [x] TypeScript Object Type exercise
```Typescript
 /* EXERCISE 1
 Intro context for the exercise:

    We are starting a small community of users. For performance
    reasons we have decided to store all users right in the code.
    This way we can provide our developers with more
    user-interaction opportunities. With user-related data, at least.
    All the GDPR-related issues will be solved some other day.
    This would be the base for our future experiments during
    these exercises.

Exercise:

    Given the data, define the interface "User" and use it accordingly.

*/

export interface User {
    name: string;
    age: number;
    occupation: string;
}

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```
5. [x] TypeScript Unions exercise
### Exercise to define the type of Person: User | Admin
```Typescript
/* EXERCISE 2

Intro:

    All 2 users liked the idea of the community. We should go
    forward and introduce some order. We are in Germany after all.
    Let's add a couple of admins.

    Initially we only had users in the in-memory database. After
    introducing Admins, we need to fix the types so that
    everything works well together.

Exercise:

    Type "Person" is missing, please define it and use
    it in persons array and logPerson function in order to fix
    all the TS errors.

*/

interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
```
# Tuesday 23 august, 2022
1. [x] Square(n) Sum exercise, using Typescript
```Typescript
export function squareSum(numbers: number[]): number {
  //1. Turn numbers to squared ^2
  //const squaredNums = Math.pow(1, 2);
  // 2. Sum the numbers once squared with .reduce()
  return numbers.reduce((prev: number, curr: number) => prev + Math.pow(curr, 2), 0);
}
```
3. [x] A Wolf In Sheep's Clothing exercise, using Typescript
```Typescript
export function warnTheSheep(queue: string[]): string {
  //1. establish the wolf location
  let wolfP = queue.indexOf('wolf');
  //2. put the conditionals to return 'go away' or 'alert the sheep'
  if(wolfP == queue.length - 1) {
    return 'Pls go away and stop eating my sheep';
} else {
  return `Oi! Sheep number ${Math.abs(wolfP + 1 - queue.length)}! You are about to be eaten by a wolf!`
}
};
```
# Wednesday 24 august, 2022
1. [x] A Rule Of Divisibility By 13 exercise, using Typescript
```Typescript
export function thirt(n: number): number {
 let remainders: number[] = [1, 10, 9, 12, 3, 4];
  let result = n
    .toString()
    .split('')
    .reverse()
    .map((c: string, i: number) => parseInt(c) * remainders[i % 6])
    .reduce((p: number, c: number) => (p += c));
  return n == result ? result : thirt(result);
}
```
3. [x] Playing With Digits exercise, using Typescript
```Typescript
export class G964 { //excuse the spanglish

    public static digPow = (n: number, p: number) => {
      let sum =
      //1. Convertir primero a string, porque solo está en num hasta ahorita
      n.toString()
      //2. Hay que convertir de string a array porque .map solo utiliza arrays
      .split('')
      //3. find a positive integer k * n = a^(n)+b^(n+1)+c^(n+2);
      .map(Number)
      //4. haz la suma de cuando ya tengas cada numero expresado a su correspondiente potencia
      .reduce((prev: number, curr: number) => prev + Math.pow(curr, p++), 0);
      //5. if the positive integer is correct, return k. always a positive number is using Math.abs(n);
      if (sum % n === 0) return sum / n; //se podría haber utilizado Math.abs() para designar el num positivo?
      //6. if not, return -1
      else return -1;
    }
}
```

# Thursday 25 august, 2022
1. [x] Declare and instantiate classes in TypeScript guided exercise, using Typescript
```Typescript
class Car implements Vehicle {
    //Properties
    private static numberOfCars: number = 0; //new static property
    private _make: string;
    private _color: string;
    private _doors: number;

    //Constructor
    constructor(make: string, color: string, doors = 4) {
        this._make = make;
        this._color = color;
        Car.numberOfCars++; //incrementa el valor del static property
        if ((doors % 2) === 0) {
            this._doors = doors;
        } else {
            throw new Error('Doors must be an even number');
        }
    }

    //Accessors
    get make() {
        return this._make;
    }
    set make(make) {
        this._make = make;
    }

    get color() {
        return 'The color of the car is ' + this._color;
    }
    set color(color) {
        this._color = color;
    }

    get doors() {
        return this._doors;
    }
    set doors(doors) {
        if((doors % 2) === 0) {
            this._doors = doors;
        } else {
            throw new Error('Doors must be an even number');
        }
    }

    //Methods
    accelerate(speed: number): string {
        return `${this.worker()} is accelerating to ${speed} MPH.`
    }
    brake(): string {
        return `${this.worker()} is braking with the standard braking system.`
    }
    turn(direction: 'left' | 'right'): string {
        return `${this.worker()} is turning ${direction}`;
    }
    protected worker(): string {
        return this._make;
    }
    public static getNumberOfCars(): number {
        return Car.numberOfCars;
    }

}
/*
let myCar1 = new Car('cool Car Company', 'blue', 2);
console.log(myCar1.color); //imprime desde el accesor
console.log(myCar1._color); //imprime desde la propiedad

let myCar3 = new Car('Galaxy Motors', 'gray');
console.log(myCar3.doors);

console.log(myCar1.accelerate(35));
console.log(myCar1.brake());
console.log(myCar1.turn('right'));
*/
// Instantiate the Car object with all parameters
let myCar1 = new Car('Cool Car Company', 'blue', 2);
// Instantiates the Car object with all parameters
let myCar2 = new Car('Galaxy Motors', 'blue', 2);
// Returns 2
console.log(Car.getNumberOfCars());

class ElectricCar extends Car { 
    //Properties unique to ElectricCar
    private _range: number;

    //Constructor
    constructor(make: string, color: string, range: number, doors = 2) {
        super(make, color, doors);
        this._range = range;
    }

    //Accessors
    get range() {
        return this._range;
    }
    set range(range) {
        this._range = range;
    }

    //Methods
    charge() {
        console.log(this.worker() + " is charging.")
    }
    brake(): string {
        return `${this.worker()} is braking with the regenerative braking system.`
    }
}

let spark = new ElectricCar('Spark Motors', 'silver', 124, 2);
let eCar = new ElectricCar('Electric Car Co.', 'black', 263);
console.log(eCar.doors); 
spark.charge(); 

console.log(spark.brake());

interface Vehicle {
    make: string;
    color: string;
    doors: number;
    accelerate(speed: number): string;
    brake(): string;
    turn(direction: 'left' | 'right'): string;
}
```

A real life example was that streaming platforms like Netflix or HBO use these properties to private screen display (screen in black).

### Second part of the Microsoft guided exercise:
```Typescript
/*  Module 5: Declare and instantiate classes in TypeScript
    Lab Start  */

/*  EXERCISE 1 */

class BuildArray {
    // TODO Define the properties
    private _items: number;
    private _sortOrder: 'ascending' | 'descending';

    // TODO Define the constructor
    constructor (items: number, sortOrder: 'ascending' | 'descending') {
    this._items = items;
    this._sortOrder = sortOrder;
    }

    // TODO Define the accessors
    get items() {
    return this._items;
    }
    set items(items) {
    this._items = items;
    }
    get sortOrder() {
    return this._sortOrder;
    }
    set sortOrder(sortOrder) {
    this._sortOrder = sortOrder;
    }

    // TODO Define the methods
    private sortDescending = (a: number, b: number) => {
        if (a > b) {
            return -1;
        } else if (b > a) {
            return 1;
        } else {
            return 0;}
    }
    private sortAscending = (a: number, b: number) => {
        if (a > b) {
            return 1;
        } else if (b > a) {
            return -1;
        } else {
            return 0; }
    }

    buildArray(): number[] {
    let randomNumbers: number[] = [];
    let nextNumber: number;
    for (let counter = 0; counter < this.items; counter++) {
        nextNumber = Math.ceil(Math.random() * (100 - 1));
        if (randomNumbers.indexOf(nextNumber) === -1) {
            randomNumbers.push(nextNumber);
        } else {
            counter--;
        }
    }
    if (this._sortOrder === 'ascending') {
        return randomNumbers.sort(this.sortAscending);
    } else {
        return randomNumbers.sort(this.sortDescending);
    } 
}


}

/*  sortDescending is a comparison function that tells the sort method how to sort numbers
    in descending order. */
let sortDescending = (a: number, b: number) => {
    if (a > b) {
        return -1;
    } else if (b > a) {
        return 1;
    } else {
        return 0; }
}

/*  sortAscending is a comparison function that tells the sort method how to sort numbers 
    in ascending order. */
let sortAscending = (a: number, b: number) => {
    if (a > b) {
        return 1;
    } else if (b > a) {
        return -1;
    } else {
        return 0;
    }
}

/*  buildArray builds an array of unique random numbers containing the number of items 
    based on the number passed to it. The sortOrder parameter determines whether to sort 
    the array in ascending or descending order. */
function buildArray(items: number, sortOrder: 'ascending' | 'descending'): number[] {
    let randomNumbers: number[] = [];
    let nextNumber: number;
    for (let counter = 0; counter < items; counter++) {
        nextNumber = Math.ceil(Math.random() * (100 - 1));
        if (randomNumbers.indexOf(nextNumber) === -1) {
            randomNumbers.push(nextNumber);
        } else {
            counter--;
        }
    }
    if (sortOrder === 'ascending') {
        return randomNumbers.sort(sortAscending);
    } else {
        return randomNumbers.sort(sortDescending);
    }

   
}

/*  TODO: Instantiate the BuildArray objects. */

let testArray1 = new BuildArray(12, 'ascending');
let testArray2 = new BuildArray(8, 'descending');

console.log(testArray1.buildArray());
console.log(testArray2.buildArray());
```

### This is what returns, the array in ascending and descending:
![image](https://user-images.githubusercontent.com/98929413/187553213-9ded50ad-08b5-4253-8772-04bd808f440c.png)

3. [x] Tile exercise, using Typescript
```Typescript
//Write a definition for a class named Tile that represents Scrabble tiles.
//The instance variables should be a string named letter and an number named value.
class Tile {
    letter: string;
    value: number;
//Write a constructor that takes parameters named letter and value and initializes the instance variables.
    constructor(letter: string, value: number;) {
        this.letter = letter;
        this.value = value;
    }
//Write a method named printTile that prints the instance variables in a reader-friendly format (not the { ... } format way).
    printTile(); {
    console.log(`

      ==================
        Letter: ${this.letter}
        Value: ${this.value}
      ==================

        `);
    }

}
```

5. [x] Time exercise, using Typescript
```Typescript
//Write a definition for the class name Time this class would be use to build a digital clock.
//This class should have 3 attributes of type number. hour, minute and second.
export class Time {
    hour: number;
    minute: number;
    second: number;
//Write a constructor that takes parameters named hour, minute and second and initializes the instance variables.
    constructor(hour: number, minute: number, second: number) {
        this.hour = hour;
        this.minute = minute;
        this.second = second;
    }
//Write a method called getInSeconds that returns a number representing the actual time in the instance represented in seconds.
    getInSeconds(): number {
        const minutes = this.hour * 60 + this.minute;
        return minutes * 60 + this.second;
    }
//Write a method named printTime that prints the instance variables in a reader-friendly format (not the { ... } format way).
    printTime() {
        console.log(` 
        ===========================
          Hours: ${this.hour}
          Minutes: ${this.minute}
          Seconds: ${this.second}
        ===========================
        `)
    }
}

//import Main from './Main';
//const main = new Main();
//main.start();
```
6. [x] Rational exercise, using Typescript
```Typescript
//Create a new class named Rational. A Rational object should have two number instance variables to store the numerator and denominator.
class Rational {
    numerator: number;
    denominator: number;
//Write a constructor for your class that takes two arguments and that uses them to initalize the instance variables.
    constructor(numerator: number, denominator: number) {
        this.numerator = numerator;
        this.denominator = denomintator;
    }
//Write a method called printRational that prints the object in some reasonable format.
    printRational {
        console.log(`${this.numerator} / ${this.denominator}`);
    }
//Write a method called invert that inverts the number by swapping the numerator and denominator. This method should modify the instance variables.
    invert {
        [numerator: number, denominator: number] = [denominator: number, numerator: number];
    }
//Write a method called toFloat that converts the rational number to a floating-point number and returns the result. This method is a pure function it does not modify the object.
    toFloat {
        return this.numerator / this.denominator;
    }
//Write method named reduce that reduces a rational number to its lowest terms by finding the greatest common divisor (GCD) of the numerator and denominator and dividing through.
    gcd(n: number, d: number): number {
        if(d == 0) return n;
        return this.gcd(d, n % d);
    }
    reduce() {
        const gcd = this.gcd(this.numerator, this.denominator);
        this.numerator = this.numerator / gcd;
        this.denominator = this.denominator /gcd;
    }
//This method should modify the instance variables. To calculate the GCD you can search for Euclidian Algorithm: GCD.
}
```
