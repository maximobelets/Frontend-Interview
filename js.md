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

#### Number methods

`number.toLocaleString()` will return a number represented by locale, without any argument will return a number separated by comma

#### String methods

`substring` const string = '_Hello World_', string.substring(1, string.length -1) // Hello World

`split` will return an array of new strings by argument

```
'Hello, World, Test'.split(',') // ["Hello", " World", " Test"]
```

`slice` will return a new part of string by represented position

```
'Hello, World'.slice(0, 5) // 'Hello'
```

#### Array methods

`at` will return element by represented index

```

['First', 'Second'].at(-1) // 'Second'

```

`find` will return first element by represented condition

```

[1, 2, 3, 7, 4, 5].find((item) => item >= 5) // 7

```

`findIndex` will return index by represented condition

```

[1, 2, 3, 7, 4, 5].findIndex((item) => item === 3) // 2

```

`join` will return a new string by represented condition

```

const arr = ['One', 'Two', 'Three'].join(' ') // 'One Two Three'

console.log(arr.join(' '));

```

#### Loops

`for` will loop through a block of code by presented number condition

```

for (let i = 0; i <= 3; i++) {
  console.log(i)
}

// 0
// 1
// 2
// 3

```