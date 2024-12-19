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

# Grasshopper - Debug sayHello [8 kyu] #25

```js
function sayHello(name) {
  return 'Hello, ' + name;
}
```

# Grasshopper - Check for factor [8 kyu] #26

```js
function checkForFactor (base, factor) {
  // code here
return base % factor ? false : true
}
```

# Are they the "same"? [6 kyu] #27

```js
function comp(array1, array2) {
  if (array1 == [] || array1 == null || array2 == [] || array2 == null)
    return false;
  if (array1.length !== array2.length) return false;
  for (let i = 0; i < array1.length; i++) {
    let isSquare = false; //Va checker si l'une des valeurs correspond dans b
for (let j = 0; j < array1.length; j++) {
      if (array1[i] * array1[i] === array2[j]) {
        console.log("r", array2[j]);
        array2.splice(j, 1);
        console.log("1:", array1);
        console.log("2", array2);
        isSquare = true;
        break;
      }
    }
    if (!isSquare) return false; //Aucun carré n'a été trouvé lors de la recherche de l'élément i
  }
  return array2.length ? false : true; //Si on est arrivé jusqu'ici, c'est que toutes les conditions ont été remplies
}
```

# You Can't Code Under Pressure #1 [8 kyu] #28

```js
function doubleInteger(i) {
  // i will be an integer. Double it and return it.
return i*2
}
```

# 5 without numbers !! [8 kyu] #29

```js
function unusualFive() {
  let str = "abcde";
  return str.length;
}
```

# Make a function that does arithmetic! [7 kyu] #30

```js
function arithmetic(a, b, operator){
  //your code here!
switch (operator) {
    case "add":
      return a + b;
      break;
    case "subtract":
      return a - b;
      break;
    case "multiply":
      return a * b;
      break;
    case "divide":
      return a/b;
      break;
    default:
      return false;
  }
}
```

# Anagram Detection [7 kyu] #31

```js
var isAnagram = function (test, original) {
  return (
    test.toLowerCase().split("").sort().join("") ==
original.toLowerCase().split("").sort().join("")
  );
};
```

# Powers of 2 [8 kyu] #32

```js
function powersOfTwo(n){
  const array = [];
  if (n < 0) return false;
  for (let i = 0 ; i < n+1 ; i++) {
    array.push(2**i)
  }
  return array;
}
```

# Sum of positive [8 kyu] #33

```js
function positiveSum(arr) {
  return arr.filter((n) => n > 0).reduce((a,n) => a + n,0);
}
```

# Exclusive "or" (xor) Logical Operator [8 kyu] #34

```js
function xor(a, b) {
  // TODO: Program Me
return a ? b ? false : true : b ? true : false;
}
```

# Small enough? - Beginner [7 kyu] #35

```js
function smallEnough(a, limit){
  return a.filter((n) => n > limit).length ? false : true;
}
```

# Reversing Words in a String [8 kyu] #36

```js
function reverse(string) {
  //your code here
return string.split(" ").reverse().join(" ");
}
```

# Count of positives / sum of negatives [8 kyu] #37

```js
function countPositivesSumNegatives(input) {
  if (!input) return [];
  const max = input.filter((n) => n > 0).length;
  const min = input.filter((n) => n < 0).reduce((a, n) => a + n, 0);
  if (max == 0 && min == 0) return []
  // your code here
return [max, min];
}
```

# Basic Mathematical Operations [8 kyu] #38

```js
function basicOp(operation, value1, value2) {
  //Code
let calcul = 0;
  switch (operation) {
    case "+":
      calcul = value1 + value2;
      break;
    case "-":
      calcul = value1 - value2;
      break;
    case "*":
      calcul = value1 * value2;
      break;
    case "/":
      calcul = value1 / value2;
      break;
    default:
      break;
  }
  return calcul
}
```

# Grasshopper - Basic Function Fixer [8 kyu] #39

```js
function addFive(num) {
  var total = num + 5
return total
}
```

# Century From Year [8 kyu] #40

```js
function century(year) {
  // Finish this :)
return Math.floor((year + 99)/100);
}
```

# Grasshopper - Terminal game combat function [8 kyu] #41

```js
function combat(health, damage) {
  // Write your code here
return health - damage < 0 ? 0 : health - damage;
}
```

# Opposites Attract [8 kyu] #42

```js
function lovefunc(flower1, flower2){
  // moment of truth
return (flower1 + flower2) % 2 ? true : false
}
```

# Convert a Boolean to a String [8 kyu] #43

```js
function booleanToString(b){
  //your code here
return String(b)
}
```

# Is the string uppercase? [8 kyu] #44

```js
String.prototype.isUpperCase = function () {
  // your code here
const abcd = "abcdefghijklmnopqrstuvwxyz".split("");
  console.log(abcd);

  return this.split("").filter((c) => abcd.includes(c)).length > 0
? false
    : true;
};
```

# Grasshopper - Messi goals function [8 kyu] #45

```js
function goals (laLigaGoals, copaDelReyGoals, championsLeagueGoals) {
  // code goes here
return laLigaGoals + copaDelReyGoals + championsLeagueGoals
}


```

# Super Duper Easy [8 kyu] #46

```js
function problem(x){
  //your code here
return x === +x ? x * 50 + 6 : "Error"
}
```

# Give me a Diamond [6 kyu] #47

```js
function diamond(n) {
  if (n <= 0 || n % 2 === 0) return null;
  let str = "";
  let counter = 1;
  let sorting = true;
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < (n - counter) / 2; j++) {
      str += " ";
    }
    for (let j = 0; j < counter; j++) {
      str += "*";
      // console.log("counter : ", counter);
    }
    str += "\n";
    if (counter >= n) {
      sorting = false;
    }
    if (sorting) counter += 2;
    else counter -= 2;
  }
  return str;
}
```

# Find the capitals [7 kyu] #48

```js
var capitals = function (word) {
  // Write your code here
return word
    .split("")
    .map((l, i) => (l === l.toUpperCase() ? i : l))
    .filter((char) => char >= 0);
};
```

# Total amount of points [8 kyu] #49

```js
function points(games) {
  let totalScore = 0;
  for (let i = 0; i < games.length; i++) {
    totalScore +=
games[i][0] - games[i][2] > 0
? 3
        : games[i][0] - games[i][2] < 0
? 0
        : 1;
  }
  return totalScore;
}
```

# Count the smiley faces! [6 kyu] #50

```js
function countSmileys(arr) {
  const validSmileys = [
    ":-)",
    ":-D",
    ":~)",
    ":~D",
    ":)",
    ":D",
    ";-)",
    ";-D",
    ";~)",
    ";~D",
    ";)",
    ";D",
  ];
  return arr.filter((smi) => validSmileys.includes(smi)).length;
}
```

# Exclamation marks series #1: Remove an exclamation mark from the end of string [8 kyu] #51

```js
function remove (string) {
  //coding and coding....
return string[string.length - 1] === "!" ? string.split("").filter((l,i) => i !== string.length - 1).join("") : string;
}
```

# Training JS #7: if..else and ternary operator [8 kyu] #52

```js
function saleHotdogs(n){
  return n < 5 ? n * 100 : n < 10 ? n * 95 : n * 90;
}
```

# Testing 1-2-3 [7 kyu] #53

```js
var number=function(array){
  //your awesome code here
return array.map((n,i) => `${i+1}: ${n}`)
}
```

# Sum of a sequence [7 kyu] #54

```js
const sequenceSum = (begin, end, step) => {
  // May the Force be with you
let sum = 0;
  for (let i = begin; i <= end; i = i + step) {
    sum += i
  }
  return sum;
};
```

