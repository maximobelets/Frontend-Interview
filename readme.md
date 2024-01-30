# Hi there!

It's a simple guide about Frontend interview with examples, hacks, tips and other features.

The main idea of this project is to find a short answer with an example on an interview question.

## Theory

JS has 7 primitive data types: `String`, `Number`, `Boolean`, `Symbol`, `Null`, `Undefined`, `BigImnt`

## JS tasks!

#### Palindrome

```
const checkPalindrome = (string) => string.split("").reverse().join("") === string;

checkPalindrome('level') // true
```