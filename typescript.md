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
