# exercicio-typescript
1-TypeScript introduction

Exercise 1:
TypeScript allows developers to add 
types to JavaScript.

Exercise 2:
JavaScript is a loosely typed language.

 2-TypeScript get Started

 Exercise 1:
tsconfig.json

3-TypeScript Simple types

Exercise 1:
Explicit
Implicit

Exercise 2:
let firstName = "Dylan";
 
 Exercise 3:
let firstName: string= "Dylan";

4-TypeScript Special types

 Exercise 1:
 let myVar: any;

Exercise 2:
let myVar: unknown;

5-TypeScript Arrays

Exercise 1:
const names: readonlystring[] =["Dylan"];

 6-TypeScript Tuples

Exercise 1:

False

Exercise 2:
let ourTuple: [string, boolean];

7-TypeScript Objects types

Exercise 1:
const car: { type: string, model: string, year:number} = {type: "Toyota",model: "Corolla"year: 2009};

Exercise 2:
const car: { type: string, model:string } = {  type: "Toyota"};

8-TypeScript Enums

Exercise 1:
enum myEnum{myFirstConst,mySecondConst};

Exercise 2:
enum myEnum{myFirstConst= "first",mySecondConst = "second"};

9-TypeScript Aliases & Interfaces

Exercise 1:

type carType = string

Exercise 2:
interfacemyInterface {myProp: string}

Exercise 3:
interface myExtInterface extends myInterface {myExtProp: number}

10-TypeScript union types

Exercise 1:
function myFunc(myVar: string|number) {console.log(myVar)}

11-TypeScript functions

Exercise 1:

function myFunc(): string{
return "Learning is Fun!";
}

Exercise 2:

function myFunc(): void{
  console.log("Learning is Fun!");
}

Exercise 3:
function myFunc(myVar1: string, myVar2: string) {
  return(myVar1 + myVar2);
}

Exercise 4:
function myFunc(myVar1: string, myVar2?: string) {
  return(myVar1 + (myVar2 || ""));
}

12- TypeScript Casting
Exercise 1:
let myVar: unknown = "Hello world!";
console.log((myVar as string).length);

Exercise 2:
let myVar: unknown = "Hello world!";
console.log((<string>myVar).length);

13-TypeScript Classes

Exercise 1:
class Person {
private name: string;

 public constructor(name: string) {
  this.name = name;
 }

public getName(): string {
  return this.name;
 }
}

14-TypeScript Basic Generics

Exercise 1:
function createPair<typeX, typeY>(x: typeX, y: typeY): [typeX, typeY] {
 return [x, y];
}
console.log(createPair<string, number>('Meaning', 42));

15-TypeScript Utilit types

Exercise 1:
interface Person {
    age: number;
    firstName: string;
    lastName: string;
}
            
let kindPerson: Partial<Person> = {};

Exercise 2:
interface Person {
    age: number;
    firstName: string;
    lastName?: string;
}
            
let kindPerson: Required<Person>= {
    age: 1800,
    firstName: "Santa",
    lastName: "Claus"
};

Exercise 3:

Record<string, number> is equivalent to { [key: string]: number }
