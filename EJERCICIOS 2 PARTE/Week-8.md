# Week challenges (Monday) 💻

1. [x] Watch Object-Oriented Programming - Resume video

- Procedural programming: program divided in a set of functions.
- Too much interdependence functions is not good in programming. Object Oriented Programming solves this.
- Units are objects. Variables, properties. Functions are methods.
- Encapsulation: Is where everything is grouped.The variables and functions. Reduce complexity and re-use code.
- Objects with no parameters, are better.
- Abstraction: Hide the complex. Show the essentials.
- Inheritance: Avoid redundant code.
- Polymorphism: Refactor "ugly" switch/case statements.
- Instance: construction of the class in the memory.
- Object: repo of data already built.

# Week challenges (Tuesday) 💻

2. [x] Develop typed functions by using TypeScript guided exercise, using Typescript

This module consisted of understanding and practicing

- Default values
- Expressions
- Optional values
- Required values

4. [x] Read Abstract Classes

Type 1: To add the properties as such. En este, la propiedad tiene que asignarse despues a la clase que se extiende también.

Type 2: The use of 'super()' to initialize it.

5. [x] Watch Abstract Classes vs Interfaces video

La diferencia entre clases abstractas e interfaces: The main difference is what they mean semantically.
Abstract classes generalize behavior. From the general to the particular.
Interfaces standarize behavior... so we do not break existing implementations.
Question to considerate: What happens if two parents have the same behavior but we want to extend or implement, which will it have?

---

- la clase abstracta puede ser extendida solo una vez y es padre-hija, siempre
- compartir comportamientos, para generalizar comportamientos
- Extender la funcionalidad general que está en la clase
- extender comportamientos generales
- ya no se pueden tener padres abstractos
- por esto se prefieren las interfaces
- solo se puede tener 1 solo padre, sea abstracto o no

---

- las interfaces se pueden implementar muchas

- definir comportamientos UNICAMENTE no da extents

- Patrón a seguir

---

- clase generica: para definir clases de tipos. revisar que los tipos de variables corran bien durante el programa
- podemos enviar tipos a la clase
- Instance: When data is assigned and called along the object.

# Week challenges (Wednesday) 💻

5. [x] Make the Deadfish Swim exercise, using Typescript (switch-case)

```Typescript
/** return the output array and ignore all non-op characters */
export function parse(data: string): number[] {
  //1. asignar variables iniciales
  let value = 0;
  //2. asignar a otra variable convertir string a array
  const result: number[] = [];
  const fishCommands = data.split('');
  //3. en un método forEach designar el switch-case para:
  fishCommands.forEach((fishCommands: string) => {
    switch (fishCommands) {
        case 'i': value++;
        break;
        case 'd': value--;
        break;
        case 's': value = Math.pow(value, 2);
        break;
        case 'o': result.push(value);
        break;
    }
  });
  // incremento de i
  // decremento de d
  // de s al cuadrado
  // de regresa los valores al array y los demuestra
  // 4. retorna resultado
  return result;
}
```

7. [x] Duplicate Encoder exercise, using Typescript

```Typescript
export function duplicateEncode(word: string){ // Success
  // lower case
  word = word.toLowerCase(); // 'success'
  // (string) | (string[]) ***
  const characters: string[] = word.split(''); // ['s','u','c','c','e','s','s']
  // iterar
  const encoded: string[] = characters.map((character) => {
    character = character.replace(/\(/g, '\\(');
    character = character.replace(/\)/g, '\\)');
    const regex = new RegExp(character, 'g');
    const found = word.match(regex) || [];
    if(found.length === 1) {
      return '(';
    }
    return ')';
  }); // [')','(',')',')','(',')',')']
  return encoded.join('');
}
```

9. [x] Find The Odd Int exercise, using Typescript

```Typescript
export const findOdd = (xs: number[]): number => {
  // happy coding!
  //1. Hay que encontrar y retornar las veces impares que aparece un num
  return xs.find((el: number, index: number, array: number[]) =>
  //2. Siempre habrá un entero que aparezca un num de veces impar
  //condition: if(xs === %2)
  array.filter((el2: number) => el2 === el).length % 2 === 1) || -1
};
```

11. [x] Which Are In? exercise, using Typescript

```Typescript
export function inArray(a1: string[], a2: string[]): string[] {

  // 0. Quitar repetidos de a1
  // 1. Recorrer a1
  // 1.1 Mientras recorro a1, filtro los elementos de a1
  // 1.1.1 Filtrar:
  // 1.1.1.1 Se quedan los elementos que son un substring de un string en a2
  // 1.1.2 sort sobre arreglo filtrado
  // 1.1.3 return de arreglo filtrado

  return [... new Set(a1)].filter((subStr:string) => {
    let result = a2.find((str:string) => str.includes(subStr));
    return result !== undefined;
  }).sort();

}

var a1 = ["live", "strong", "lyal", "lysh", "arp"]
var a2:string[] = ["lively", "alive", "harp", "sharp", "armstrong"]
//   r = ["live", "strong", "arp"] ==> ["arp","live", "strong" ]


console.log(inArray(a1, a2));
```

# Week challenges (Thursday) 💻

9. [x] Define generics in TypeScript guided exercise, using Typescript
10. [x] Generics exercise, using Typescript

Node.ts

```Typescript
export default class Node<T> {
  public data: T;
  public next: Node<T> | null = null;

  constructor(data: T) {
    this.data = data;
  }
}
```

LinkedLists.ts

```Typescript
import Node from './Node';
export default class LinkedList<T> {
  private head: Node<T> | null = null;
  private length: number = 0;

  get size(): number {
    return this.length;
  }

  public addFirst(value: T) {
    //1. primero recorre la lista, para agregar el primero
    if (this.head === null) {
      this.add(value);
    } else {
      let node = new Node(value);
      node.next = this.head;
      this.head = node;
      this.length++;
    }

  }

  public add(data: T) {
    if (this.head === null) {
      this.head = new Node(data);
    } else {
      let temp = this.head;
      while (temp.next !== null) {
        temp = temp.next;
      }
      temp.next = new Node(data);
    }
    this.length++;
  }

  public remove() {
    if (this.head !== null) {
      this.head = this.head.next;
      this.length--;
    }
  }

  public toString(): string {
    if (this.length === 0) return '[]';
    let data = '';
    let node = this.head;
    while (node !== null) {
      data = `${data}${node.data},`;
      node = node.next;
    }
    data = data.slice(0, -1);
    return `[${data}]`;
  }

  public removeLast(): void {
    if (this.head !== null) {
      // 1. primero recorre a la lista, para remover el último
      let node = this.head;
      let previous: Node<T> = node;
      while (node.next !== null) {
        previous = node;
        node = node.next
      }
      //2. si ya llegó al lugar next = null
      previous.next = null
      this.length--;
    }
  }
}
```

Program run/start:
![image](https://user-images.githubusercontent.com/98929413/190287546-091d8f73-1003-465e-8015-cd3b45bc1191.png)

12. [x] Upload resume
