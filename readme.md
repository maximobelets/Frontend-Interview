# Hi there!

It's a simple guide about Frontend interview with examples, hacks, tips and other features.

The main idea of this project is to find a short answer with an example on an interview question.

## Theory

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

#### String methods

substring | const string = '_Hello World_', string.substring(1, string.length -1) // Hello World

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

const testString: string = 'typescript';

const number: number = 1;

const trueOrFalse: boolean = true;

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
