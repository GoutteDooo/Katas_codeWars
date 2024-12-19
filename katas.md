# Third Angle of a Triangle [8 kyu] #1

```js
function otherAngle(a, b) {
  return 180 - a - b;
}
```

# Hex to Decimal [8 kyu] #2

```js
function hexToDec(hexString) {
  //your code here
return Number("0x" + hexString)
    ? Number("0x" + hexString)
    : -Number("0x" + hexString.slice(1));
}
```

# Summing a number's digits [7 kyu] #3

```js
function sumDigits(number) {
  return number
    .toString()
    .split("")
    .filter((char) => char >= 0 && char < 10)
    .map((n) => +n)
    .reduce((a, n) => a + n, 0);
}
```

# Form The Minimum [7 kyu] #4

```js
function minValue(values) {
  //your code here
const counts = values.reduce((a, n) => {
    a[n] = (a[n] || 0) + 1;
    return a;
  }, {});
  return +values
    .sort((a, b) => a - b)
    .filter((n, i, self) => self.indexOf(n) === i)
    .map((n) => n.toString())
    .join("");
}
```

# Training JS #1: create your first JS function and print "Hello World!" [8 kyu] #5

```js
//refer to the example and write your first JS function
function helloWorld() {
  let str = "Hello World!";
  
  console.log(str);
}
```

# Multiplication table [6 kyu] #6

```js
multiplicationTable = function (size) {
  // insert code here
const array = [];
  let multiplicateur = 1;
  for (let i = 0; i < size; i++) {
    array.push([]);
    for (let j = 0; j < size; j++) {
      array[i].push(multiplicateur * (j + 1));
    }
    multiplicateur++;
  }
  return array;
};

```

# Tribonacci Sequence [6 kyu] #7

```js
function tribonacci(signature, n) {
  //your code here
if (n === 0) return [];
  if (n === 1) return [signature[0]];
  // if (n === 2) return [signature[0] + signature[1]];
if (n < 3) return signature.reduce((a, n) => a + n, 0);
  for (let i = 0; i < n - 3; i++) {
    let nextValue = signature
      .filter((n, i) => i >= signature.length - 3)
      .reduce((a, n) => a + n, 0);
    signature.push(nextValue);
  }
  return signature;
}
```

# Simple Fun #176: Reverse Letter [7 kyu] #8

```js
function reverseLetter(str) {
  const acceptedLetters = "abcdefghijklmnopqrstuvwxyz".split("");
  console.log(acceptedLetters[2]);

  //coding and coding..
return str
    .split("")
    .filter((char, i) => char == acceptedLetters.find((l) => l == char))
    .reverse()
    .join("");
}
```

# Find the position! [8 kyu] #9

```js
function position(letter){
  //Write your own Code!
return "Position of alphabet: " + String(letter.charCodeAt(0) - 96);
}
```

# Name Shuffler [8 kyu] #10

```js
function nameShuffler(str){
  //Shuffle It
return str.split(" ").reverse().join(" ");
}
```

# Descending Order [7 kyu] #11

```js
function descendingOrder(n) {
  return +n
    .toString()
    .split("")
    .sort((a, b) => b - a)
    .join("");
}
```

# Find the middle element [7 kyu] #12

```js
function gimme(triplet) {
  //trouver le gimme
const gimme = [...triplet].sort((a, b) => a - b)[1];

  //le retourner
return triplet.findIndex((n) => n === gimme);
}
```

# Title Case [6 kyu] #13

```js
function titleCase(title, minorWords = null) {
  if (minorWords) {
    minorWords = minorWords.split(" ");
    console.log(minorWords);
  }
  title = title.split(" ");
  console.log(title);
  for (let i = 0; i < title.length; i++) {
    if (minorWords) {
      // Si minorWords
for (let j = 0; j < minorWords.length; j++) {
        if (minorWords[j].toLowerCase() === title[i].toLowerCase() && i) {
          title[i] = title[i].toLowerCase();
          break;
        } else
title[i] =
title[i].charAt(0).toUpperCase() + title[i].slice(1).toLowerCase();
      }
    } else {
      //Si pas de minorWords, on fait la même
title[i] =
title[i].charAt(0).toUpperCase() + title[i].slice(1).toLowerCase();
    }
  }
  return title.join(" ");
}
```

# Plural [8 kyu] #14

```js
function plural(n) {
  // ...
return n == 1 ? false : true
}
```

# RaNDoM CAsE [7 kyu] #15

```js
function randomCase(x) {
  // Code your solution here
return x
    .split("")
    .map((l) => (Math.random() < 0.5 ? l.toLowerCase() : l.toUpperCase()))
    .join("");
}
```

# Beginner - Reduce but Grow [8 kyu] #16

```js
function grow(x){
  return x.reduce((a,n) => a = a * n, 1)
}
```

# Calculate average [8 kyu] #17

```js
function findAverage(array) {
  // your code here
if (!array) return [];
  if (!array.length) return 0;
  const length = array.length;
  return array.reduce((a, n) => (a = a + n), 0) / length;
}
```

# get character from ASCII Value [8 kyu] #18

```js
function getChar(c) {
  // ...
return String.fromCharCode(c);
}
```

# Reverse List Order [8 kyu] #19

```js
function reverseList(list) {
  return list.reverse()
}
```

# MakeUpperCase [8 kyu] #20

```js
function makeUpperCase(str) {
  // Code here
return str.split("").map((char) => char.toUpperCase()).join("");
}
```

# No zeros for heros [8 kyu] #21

```js
function noBoringZeros(n) {
  // your code
const array = n.toString().split("");
  for (let i = array.length - 1; i >= 0; i--) {
    if (array[i] === "0") {
      array.splice(i, 1);
    } else {
      break;
    }
  }
  return +array.join("");
}
```

# Is this a triangle? [7 kyu] #22

```js
function isTriangle(a, b, c) {
  if (a + b + c < 0) return false;
  return [a, b, c].sort((a, b) => b - a)[0] >=
    [a, b, c].sort((a, b) => b - a)[1] + [a, b, c].sort((a, b) => b - a)[2]
    ? false
    : true;
}
```

# Grasshopper - Terminal game move function [8 kyu] #23

```js
function move (position, roll) {
  // return the new position
return position + roll * 2
}
```

# Function 2 - squaring an argument [8 kyu] #24

```js
// Write the "square"-function here
function square(number) {
  return number * number;
}
```

