# Hi there!

It's a simple guide about Frontend interview with examples, hacks, tips and other features.

The main idea of this project is to find a short answer with an example on an interview question.

## Theory

### Computer Science

### Data structures

Array, Stack, Queue, Graph, Linked List and more.

#### HTTP Request

Methods

GET - for taking data from the server.

HEAD - the same GET request but without body part.

POST - this request sends a data to the server.

PUT - for replace all data by request data.

DELETE - for delete some data.

OPTIONS - for getting the server information. For example, all supported methods.

PATCH - for change a piece of data.

TRACE - for diagnostic, debugging connection.

CONNECT - for creation a two-way tunnel with a server. 

#### Data types

JS has 8 data types: `String`, `Number`, `Boolean`, `Symbol`, `Null`, `Undefined`, `BigImnt`, `Object`

All of these are primitive except `Object`

#### Maths operations

How to know do wo have remainder from division, use % operator

```
console.log(5 % 2) // 1
console.log(4 % 2) // 0
```

#### Element methods

`scrollTo(0, 0)` will scroll to the represented coordinates (0, 0)

#### String methods

substring | const string = '_Hello World_', string.substring(1, string.length -1) // Hello World

#### Array methods

`at` will return element by represented index

```

['First', 'Second'].at(-1) // 'Second'

```

`find` will return first element by represented condition

```

[1, 2, 3, 7, 4, 5].find((item) => item >= 5) // 7

```

## JS tasks!

#### Palindrome

```
const checkPalindrome = (string) => string.split("").reverse().join("") === string;

checkPalindrome('level') // true
```

#### Remove duplicates from an array

```
const removeDuplicates = (arr) => arr.filter((item, index) => arr.indexOf(item) === index);

removeDuplicates(['A', 'B', 'C', 'A']) // ['A', 'B', 'C']
```

#### Find the sum of an array of numbers

```
[1, 1, 2, 3].reduce((acc, val) => acc + val) // 7

```

## TypeScript

#### Basic types

const testString: string = 'typescript';

const number: number = 1;

const trueOrFalse: boolean = true;

#### Readonly type

```
interface IBook {
    book: string,
    readonly pages: number
}

const testBook: IBook = {
  book: 'Test Book',
  pages: 100,
}

testBook.pages = 200; // Cannot assign to 'pages' because it is a read-only property
```
#### Array types

const arr: Array<number> = [1, 2, 3];

const arr: string[] = ['test', 'string'];

#### Function type

```
const getCar = (model: string, year: number): string => `Model: ${model}, Year: ${year}`;
```

#### enum

```
const enum Languages {
    JavaScript = 'js',
    TypeScript = 'ts',
    Java = 'java',
}

interface IDeveloper {
    role: string,
    language: Languages
}

const developer: IDeveloper = {
    role: 'developer',
    language: Languages.TypeScript
}

console.log(developer) // {role: "developer", language: "ts"}

```

#### How to unite types

```
type Car = {
    model: string;
    year: number;
}

type isNewCar = {
    isNewCar: boolean
};

const testCar: Car & isNewCar = { model: 'TestCar', year: 1994, isNewCar: false }

```

#### Generics

```

const genericFunc = <T>(data: T): T => {
    return data
}

genericFunc<number>(123)

interface ICar<M, Y> {
    model: M,
    year: Y,
}

const testCar: ICar<string, number> = {
    model: 'TestCar',
    year: 1994,
}

```

#### Utility Types

### Omit, Pick, Record

```

interface ICar {
    model: string,
    year: number,
    isNewCar: boolean,
}

interface ITestCar extends Omit<ICar, 'isNewCar'> {}

interface ICarModel extends Pick<ICar, 'model'> {}

interface ICarModel extends Partial<ICar> {} // To make all types optional

interface ICarModel extends Required<ICar> {} // To make all types required

type TypeTestCarRecord = Record<'model' | 'year', string | number>

const car: ITestCar = {
    model: 'testCar',
    year: 1994,
}

const car: ICarModel = {
    model: 'testCar',
}

```

