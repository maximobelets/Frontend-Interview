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

```
const arr: Array<number> = [1, 2, 3];

const arr: string[] = ['test', 'string'];
```

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
#### keyof

```

type Car = {
    model: string;
    year: number;
}

type CarKeys = keyof Car; // ("model" | "year")

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

interface Car<M, Y> {
    model: M,
    year: Y,
}

const testCar: Car<string, number> = {
    model: 'TestCar',
    year: 1994,
}

```

#### Utility Types

#### Omit, Pick, Record

Let's create a simple interface for car

```
interface Car {
    model: string,
    year: number,
    isNewCar: boolean,
}
```

Let's pick only __model__ from __Car__

```
type CarModel = Pick<Car, 'model'>;
```

Let's remove __isNewCar__ from __Car__

```
type CarModel = Omit<Car, 'isNewCar'>;
```

Let's make all keys are optional

```
type PartialCar = Partial<Car>;
```

Let's make all keys are required

```
interface Car {
    model: string,
    year: number,
    isNewCar?: boolean,
}

type PartialCar = Required<Car>;
```
