## JS tasks!

#### Sort an array of numbers in ascending order

```
const arr = [10, 7, 3, 1]

arr.sort((a, b) => a -b) // [1, 3, 7, 10]
```


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