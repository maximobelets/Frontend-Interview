# Hi there!

It's a simple guide about Frontend interview with examples, hacks, tips and other features.

The main idea of this project is to find a short answer with an example on an interview question.

## Theory

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