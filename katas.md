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

# Find Maximum and Minimum Values of a List [8 kyu] #55

```js
var min = function(list){
    
    return list.sort((a,b) => a - b)[0];
}

var max = function(list){
    
    return list.sort((a,b) => b - a)[0];
}
```

# Opposite number [8 kyu] #56

```js
function opposite(number) {
  //your code here
return -number
}
```

# Are You Playing Banjo? [8 kyu] #57

```js
function areYouPlayingBanjo(name) {
  // Implement me
return name[0].toLowerCase() === "r" ? `${name} plays banjo` : `${name} does not play banjo`;
}
```

# Sort Numbers [7 kyu] #58

```js
function solution(nums){
  return nums ? nums.sort((a,b) => a - b) : [];
}
```

# Switch it Up! [8 kyu] #59

```js
function switchItUp(number){
//Write your own Code!
const base = {
    "0":"Zero",
    "1":"One",
    "2":"Two",
    "3":"Three",
    "4":"Four",
    "5":"Five",
    "6":"Six",
    "7":"Seven",
    "8":"Eight",
    "9":"Nine",
  }
  return base[number];
}
```

# What's the real floor? [8 kyu] #60

```js
function getRealFloor(n) {
  return n < 14 ? n < 1 ? n : n-1 : n - 2;
}
```

# Sort and Star [8 kyu] #61

```js
function twoSort(s) {
  return s.sort().map((word) =>
word
      .split("")
      .map((l, i) => (i < word.length - 1 ? (l = l + "***") : l))
      .join("")
  )[0];
}
```

# Your order, please [6 kyu] #62

```js
function order(words){
  // ...
if (!words.length) return "";
  let letters = words.split(" ").map((word) => word.split("").map((l) => +l ? +l : l));
  let indexToFind = 0;
  for (let i = 0 ; i < letters.length ; i++) {
    let temp = "";
    for (let j = 0 ; j < letters[i].length ; j++) {
      if (letters[i][j] === indexToFind+1) {
        temp = letters[indexToFind];
        letters[indexToFind] = letters[i];
        letters[i] = temp;
        indexToFind++;
        i = 0;
        continue;
      }
    }
  }
  return letters.map((word) => word.join("")).join(" ");
}
```

# Sum The Strings [8 kyu] #63

```js
function sumStr(a,b) {
  return String(+a + +b);
}
```

# Keep Hydrated! [8 kyu] #64

```js
function litres(time) {
  return Math.floor(time * 0.5);
}
```

# Filter out the geese [8 kyu] #65

```js
function gooseFilter (birds) {
  var geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
  const array = []
  for (let i = 0 ; i < birds.length ; i++) {
    let isGeese = false;
    for (let j = 0 ; j < geese.length ; j++) {
      if (geese[j] === birds[i]) {isGeese = true;}
    }
    if (!isGeese) array.push(birds[i])
  }
  
  // return an array containing all of the strings in the input array except those that match strings in geese
return array;
};
```

# Parse nice int from char problem [8 kyu] #66

```js
function getAge(inputString){
// return the girl's correct age as an integer. Happy coding :) 
return Number(inputString[0])
}
```

# Square(n) Sum [8 kyu] #67

```js
function squareSum(numbers){
  return numbers.reduce((a,n) => a + n*n,0)
}
```

# Difference of Volumes of Cuboids [8 kyu] #68

```js
function findDifference(a, b) {
  //loading...
return Math.abs(a.reduce((a, n) => a * n, 1) - b.reduce((a, n) => a * n, 1));
}
```

# I love you, a little , a lot, passionately ... not at all [8 kyu] #69

```js
function howMuchILoveYou(nbPetals) {
  const phrases = [
    "I love you",
    "a little",
    "a lot",
    "passionately",
    "madly",
    "not at all",
  ];

  return phrases[(nbPetals - 1) % 6];

  // your code
}
```

# Count the Digit [7 kyu] #70

```js
function nbDig(n, d) {
  // your code
//créer une boucle pour implémenter le tableau des puissances
let counter = 0;
  let array = [];
  for (let i = 1; i < n + 1; i++) {
    array.push(i * i);
  }
  array = array.map((n) => n.toString());
  for (let i = 0; i < array.length; i++) {
    for (let j = 0; j < array[i].length; j++) {
      counter += array[i][j] === String(d) ? 1 : 0;
    }
  }
  //une fois le tableau créé, rechercher le digit dans chaque élément (string), et incrémenter le compteur
// retourner le compteur
return d === 0 ? counter + 1 : counter;
}
```

# Rot13 [5 kyu] #71

```js

function rot13(message) {
  //your code here
return message
    .split("")
    .map((l) => {
      if (l.match(/[^a-zA-Z]/, l)) return l;
      if (l === l.toLowerCase()) return ((l.charCodeAt(0) - 97 + 13) % 26) + 97;
      if (l === l.toUpperCase()) return ((l.charCodeAt(0) - 65 + 13) % 26) + 65;
    })
    .map((n) => {
      if (n === Number(n)) return String.fromCharCode(n);
      return n;
    })
    .join("");
}
```

# Is he gonna survive? [8 kyu] #72

```js
function hero(bullets, dragons){
  return bullets / 2 < dragons ? false : true;
}

```

# Will you make it? [8 kyu] #73

```js
const zeroFuel = (distanceToPump, mpg, fuelLeft) => {
  // TODO
return distanceToPump <= mpg * fuelLeft ? true : false;
};


```

# Product of consecutive Fib numbers [5 kyu] #74

```js
function productFib(prod) {
  let tempF = 1, //f0
lastF = 1, //f1
currentF = lastF + tempF; //f2
let saveMin = lastF * tempF;
  let saveMax = currentF * lastF;
  while (saveMax < prod) {
    if (currentF * lastF < prod) {
      saveMin = currentF * lastF;
    } else {
      saveMax = currentF * lastF;
      break;
    }
    tempF = currentF; //tempF prend f(n)
console.log(tempF);

    currentF = currentF + lastF; //f(n+1) = f(n) + f(n-1)
lastF = tempF; //f(n-1) = f(n)
// console.log(saveMin);
  }

  return saveMax === prod ? [tempF, currentF, true] : [tempF, currentF, false];
}
```

# Sum Mixed Array [8 kyu] #75

```js
function sumMix(x) {
  return x.map((ele) => +ele).reduce((a,n) => a + n, 0);
}
```

# Count by X [8 kyu] #76

```js
function countBy(x, n) {
  return Array.from({ length: n }, (_, i) => (i + 1) * x);
}
```

# Quarter of the year [8 kyu] #77

```js
const quarterOf = (month) => {
  // Your code here
return month < 4
? 1
    : month < 7
? 2
    : month < 10
? 3
    : month < 13
? 4
    : false;
};
```

# Sort the odd [6 kyu] #78

```js
function sortArray(array) {
  // Return a sorted array.
const arrayOdd = array
    .map((n) => (n % 2 ? n : ""))
    .filter((ele) => ele === Number(ele))
    .sort((a, b) => a - b);
  let counter = 0;
  for (let i = 0; i < array.length; i++) {
    if (array[i] % 2) {
      array[i] = arrayOdd[counter];
      counter++;
    }
  }
  return array;
}
```

# Thinkful - Logic Drills: Traffic light [8 kyu] #79

```js
function updateLight(current) {
  //your code here!
return current == "green" ? "yellow" : current == "yellow" ? "red" : "green";
}
```

# Find the stray number [7 kyu] #80

```js
function stray(numbers) {
  return Number(
    Object.entries(
      numbers.reduce((a, n) => {
        a[n] = (a[n] | 0) + 1;
        return a;
      }, {})
    ).find(([key, value]) => value === 1)[0]
  );
}
```

# Two to One [7 kyu] #81

```js
function longest(s1, s2) {
  // your code
return s1
    .concat(s2)
    .split("")
    .filter((char, i, self) => self.indexOf(char) === i)
    .sort()
    .join("");
}
```

# Counting sheep... [8 kyu] #82

```js
function countSheeps(sheeps) {
  return sheeps.filter((sheep) => sheep == true).length;
}
```

# Mumbling [7 kyu] #83

```js

function accum(s) {
  if (!s.length) return false;
  let currentLetter = "";
  let newString = "";
  for (let i = 0; i < s.length; i++) {
    currentLetter = s[i];
    console.log("currentLetter : ", currentLetter, " i : ", i);

    for (let j = 0; j < i + 1; j++) {
      newString +=
j == 0 ? currentLetter.toUpperCase() : currentLetter.toLowerCase();
      console.log("newString : ", newString, ", j = ", j);
    }
    if (i < s.length - 1) newString += "-";
  }
  return newString;
}
```

# Beginner Series #2 Clock [8 kyu] #84

```js
function past(h, m, s){
  return h * 3600 * 1000 + m * 60 * 1000 + s * 1000;
}
```

# Keep up the hoop [8 kyu] #85

```js

function hoopCount(n) {
  //your code goes here
return n > 9 ? "Great, now move on to tricks" : "Keep at it until you get it";
}
```

# Isograms [7 kyu] #86

```js
function isIsogram(str) {
  //...
const strSorted = str.toLowerCase().split("").sort().join("");
  for (let i = 0; i < str.length - 1; i++) {
    if (strSorted[i].toLowerCase() == strSorted[i + 1].toLowerCase())
      return false;
  }
  return true;
}
```

# Reverse words [7 kyu] #87

```js
function reverseWords(str) {
  // Go for it
return str
    .split(" ")
    .map((words) => words.split("").reverse().join(""))
    .join(" ");
}

```

# Ones and Zeros [7 kyu] #88

```js
const binaryArrayToNumber = (arr) => {
  // your code
return arr
    .reverse()
    .map((b, i) => (b = b == 1 ? (b + 1) ** i : 0))
    .reverse()
    .reduce((a, n) => a + n, 0);
};
```

# altERnaTIng cAsE <=> ALTerNAtiNG CaSe [8 kyu] #89

```js
String.prototype.toAlternatingCase = function () {
  // Define your method here :)
return this.split("")
    .map((l) => {
      if (l == l.toUpperCase()) return l.toLowerCase();
      if (l == l.toLowerCase()) return l.toUpperCase();
    })
    .join("");
};
```

# Remove the minimum [7 kyu] #90

```js
function removeSmallest(numbers) {
  if (!numbers.length) return [];
  let smallest = numbers[0];
  return numbers
    .map((n) => {
      smallest = smallest < n ? smallest : n;

      return n;
    })
    .filter((n, i, s) => s.indexOf(smallest) !== i);
}
```

# Sum of odd numbers [7 kyu] #91

```js
function rowSumOddNumbers(n) {
  // TODO
let length = 0;
  for (let i = 1; i < n + 1; i++) {
    length += i;
  }
  //length définie, on prend length impairs
let result = 0;
  let currentOdd = 0;
  //Générer la liste de nombres impaires
for (let i = 1; i < length + 1; i++) {
    currentOdd = i + i - 1;
    result += i > length - n ? currentOdd : 0;
  }

  return result;
}
```

# Convert a String to a Number! [8 kyu] #92

```js
const stringToNumber = function(str){
  // put your code here
return +str;
}
```

# Count characters in your string [6 kyu] #93

```js

function count(string) {
  // TODO
return string.split("").reduce((a, l) => {
    a[l] = (a[l] | 0) + 1;
    return a;
  }, {});
}
```

# Throwing Darts [6 kyu] #94

```js
function scoreThrows(radii) {
  let count = 0;
  let strike = 0;
  if (!radii.length) return 0;
  for (let i = 0; i < radii.length; i++) {
    if (radii[i] < 5) {
      count += 10;
      strike++;
    } else if (radii[i] <= 10) {
      count += 5;
    }
  }
  count += strike == radii.length ? 100 : 0;

  return count;
}
```

# Calculate BMI [8 kyu] #95

```js
function bmi(w, h) {
  const bmi = w / (h * h);
  return bmi <= 18.5
? "Underweight"
    : bmi <= 25
? "Normal"
    : bmi <= 30
? "Overweight"
    : "Obese";
}
```

# Welcome! [8 kyu] #96

```js
function greet(language) {
  const database = [
    ["english", "Welcome"],
    ["czech", "Vitejte"],
    ["danish", "Velkomst"],
    ["dutch", "Welkom"],
    ["estonian", "Tere tulemast"],
    ["finnish", "Tervetuloa"],
    ["flemish", "Welgekomen"],
    ["french", "Bienvenue"],
    ["german", "Willkommen"],
    ["irish", "Failte"],
    ["italian", "Benvenuto"],
    ["latvian", "Gaidits"],
    ["lithuanian", "Laukiamas"],
    ["polish", "Witamy"],
    ["spanish", "Bienvenido"],
    ["swedish", "Valkommen"],
    ["welsh", "Croeso"],
  ];
  return database.filter((e) => e[0] === language).length
? database.filter((e) => e[0] === language)[0][1]
    : "Welcome";
}
```

# Transportation on vacation [8 kyu] #97

```js
function rentalCarCost(d) {
  let off = 0;
  if (d > 2) {
    if (d > 6) off = -50;
    else off = -20;
  }
  return d * 40 + off;
}
```

# How good are you really? [8 kyu] #98

```js
function betterThanAverage(classPoints, yourPoints) {
  // Your code here
const mates = classPoints.length;
  return yourPoints > classPoints.reduce((a, n) => a + n, 0) / mates
? true
    : false;
}

```

# Correct the mistakes of the character recognition software [8 kyu] #99

```js
function correct(string) {
  // your code here
return string.replace(/[015]/g, (char) => {
    if (char == 0) return "O";
    if (char == 1) return "I";
    if (char == 5) return "S";
  });
}
```

# Bingo Card [6 kyu] #100

```js
function getCard() {
  const bingo = [];
  let m = 0;
  let counter = 0;
  while (bingo.length < 24) {
    let randomNumber;
    if (counter < 5) randomNumber = Math.floor(Math.random() * 15 + 1 + 15 * 0);
    else if (counter < 10)
      randomNumber = Math.floor(Math.random() * 15 + 1 + 15 * 1);
    else if (counter < 14)
      randomNumber = Math.floor(Math.random() * 15 + 1 + 15 * 2);
    else if (counter < 19)
      randomNumber = Math.floor(Math.random() * 15 + 1 + 15 * 3);
    else if (counter < 24)
      randomNumber = Math.floor(Math.random() * 15 + 1 + 15 * 4);
    console.log("random : ", randomNumber, " bingo : ", bingo);

    if (
      !bingo.includes(`B${randomNumber}`) &&
!bingo.includes(`I${randomNumber}`) &&
!bingo.includes(`N${randomNumber}`) &&
!bingo.includes(`G${randomNumber}`) &&
!bingo.includes(`O${randomNumber}`)
    ) {
      console.log("inséré");

      // Vérifier si le nombre est déjà dans le tableau
if (bingo.length < 5) bingo.push("B" + randomNumber);
      else if (bingo.length < 10) bingo.push("I" + randomNumber);
      else if (bingo.length < 14) bingo.push("N" + randomNumber);
      else if (bingo.length < 19) bingo.push("G" + randomNumber);
      else if (bingo.length < 25) bingo.push("O" + randomNumber);
      counter++;
    }
  }

  return bingo;
}
```

# Complete The Pattern #1 [7 kyu] #101

```js
function pattern(n) {
  var output = "";
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < i + 1; j++) {
      output += i + 1;
    }
    if (i + 1 !== n) output += "\n";
  }
  return output;
}
```

# Number of People in the Bus [7 kyu] #102

```js
var number = function (busStops) {
  let peopleIn = 0;
  for (let i = 0; i < busStops.length; i++) {
    peopleIn += busStops[i][0] - busStops[i][1];
  }
  return peopleIn;
};
```

# Printer Errors [7 kyu] #103

```js
function printerError(s) {
  const length = s.length;
  let countError = s
    .split("")
    .map((char) => char > "m")
    .filter((bool) => bool).length;
  return `${countError}/${length}`;
}
```

# Convert a Number to a String! [8 kyu] #104

```js
function numberToString(num) {
  // Return a string of the number here!
return String(num);
}
```

# All Star Code Challenge #18 [8 kyu] #105

```js
function strCount(str, letter) {
  //code here
return str.split("").filter((l) => l == letter).length;
}
```

# String repeat [8 kyu] #106

```js
function repeatStr(n, s) {
  let newString = "";
  for (let i = 0; i < n; i++) {
    newString += s;
  }
  return newString;
}
```

# Equal Sides Of An Array [6 kyu] #107

```js
function findEvenIndex(arr) {
  for (let i = 0; i < arr.length; i++) {
    const sumLeft = arr.reduce((a, n, j) => (j < i ? a + n : a), 0);
    const sumRight = arr.reduce((a, n, j) => (j > i ? a + n : a), 0);
    console.log("i : ", i, sumLeft, sumRight);
    if (sumLeft === sumRight) return i;
  }
  return -1;
}
```

# Beginner Series #4 Cockroach [8 kyu] #108

```js
function cockroachSpeed(s) {
  //Good Luck!
return Math.floor((s / 3600) * 100000);
}
```

# Vowel Count [7 kyu] #109

```js
function getCount(str) {
  return str.match(/[aeiou]/g) ? str.match(/[aeiou]/g).length : 0;
}
```

# Area or Perimeter [8 kyu] #110

```js
const areaOrPerimeter = function(l , w) {
  return l == w ? l*w : l*2 + w*2;
};
```

# The Feast of Many Beasts [8 kyu] #111

```js
function feast(beast, dish) {
  return beast[0] == dish[0] && beast[beast.length-1] == dish[dish.length-1] ? true : false;
}
```

# Simple multiplication [8 kyu] #112

```js
function simpleMultiplication(number) {
  // your code........
return number % 2 == 0 ? number * 8 : number *9;
}

```

# Grasshopper - Grade book [8 kyu] #113

```js
function getGrade (s1, s2, s3) {
  const moyenne = (s1+s2+s3) / 3;
  if (moyenne < 60) return "F";
  if (moyenne < 70) return "D";
  if (moyenne < 80) return "C";
  if (moyenne < 90) return "B";
  return "A";
  
}
```

# List Filtering [7 kyu] #114

```js
function filter_list(l) {
  // Return a new array with the strings filtered out
return l.filter((n) => typeof n == "number");
}
```

# Will there be enough space? [8 kyu] #115

```js
function enough(cap, on, wait) {
  return on + wait - cap < 0 ? 0 : on + wait - cap;
}

```

# Write Number in Expanded Form [6 kyu] #116

```js
function expandedForm(num) {
  // Your code here
num = num.toString().split("");
  let result = [];
  for (let i = 0; i < num.length; i++) {
    if (num[i] !== "0") result.push(num[i] + "0".repeat(num.length - i - 1));
  }
  return result.join(" + ");
}
```

# Volume of a Cuboid [8 kyu] #117

```js
class Kata {
  static getVolumeOfCuboid(length, width, height) {
    return length * width * height;
  }
}
```

# Beginner Series #1 School Paperwork [8 kyu] #118

```js
function paperwork(n, m) {
  return n < 0 || m < 0 ? 0 : n * m;
}
```

# Twice as old [8 kyu] #119

```js
function twiceAsOld(dadYearsOld, sonYearsOld) {
  // your code here
let counter = 0;
  if (dadYearsOld > sonYearsOld * 2) {
    while (dadYearsOld > sonYearsOld * 2) {
      dadYearsOld--;
      counter++;
    }
  } else {
    while (dadYearsOld < sonYearsOld * 2) {
      dadYearsOld++;
      counter++;
    }

  }
  return counter;
}
```

# Remove String Spaces [8 kyu] #120

```js
function noSpace(x) {
  return x.replace(/ /g, "");
}
```

# You only need one - Beginner [8 kyu] #121

```js
function check(a, x) {
  // your code here
return a.find((n) => n === x) == undefined ? false : true;
}
```

# Consecutive strings [6 kyu] #122

```js
function longestConsec(strarr, k) {
  let result = "";
  if (k < 0) return result;
  for (let i = 0; i < strarr.length - k + 1; i++) {
    const consecutiveString = strarr.slice(i, k + i).join("");
    result =
result.length < consecutiveString.length ? consecutiveString : result;
  }

  return result;
}
```

# String ends with? [7 kyu] #123

```js
function solution(str, ending) {
  // TODO: complete
return str.endsWith(ending);
}
```

# Mexican Wave [6 kyu] #124

```js
function wave(str) {
  // Code here
const result = [];
  for (let i = 0; i < str.length; i++) {
    if (str[i] === " ") continue;
    result.push(str.slice(0, i) + str[i].toUpperCase() + str.slice(i + 1));
  }
  return result;
}
```

# Unique In Order [6 kyu] #125

```js
var uniqueInOrder = function (iterable) {
  //your code here - remember iterable can be a string or an array
if (!Array.isArray(iterable)) iterable = iterable.split("");
  if (iterable.length == 0) return [];
  if (typeof iterable[0] === "number")
    return iterable
      .join("")
      .toString()
      .match(/(\w)(?!\1)/g)
      .map((n) => (n = Number(n)));
  else
return iterable
      .join("")
      .toString()
      .match(/(\w)(?!\1)/g);
};
```

# Detect Pangram [6 kyu] #126

```js
function isPangram(string) {
  console.log(string.toLowerCase().replace(/ /g, "").split("").sort());
  const alphabet = Array.from({ length: 26 }, (_, i) =>
String.fromCharCode(97 + i)
  );

  return alphabet.every((letter) =>
string
      .toLowerCase()
      .replace(/ /g, "")
      .split("")
      .reduce((a, l, i) => {
        a[l] = (a[l] || 0) + 1;
        return a;
      }, {})
      .hasOwnProperty(letter)
  );
}
```

# Even or Odd [8 kyu] #127

```js
function evenOrOdd(number) {
  return number % 2 ? "Odd" : "Even";
}
```

# Break camelCase [6 kyu] #128

```js
function solution(string) {
  return string.replace(/[A-Z]/g, (char) => " " + char);
}
```

# Removing Elements [8 kyu] #129

```js

function removeEveryOther(arr) {
  //your code here
return arr.filter((n, i) => i % 2 == 0);
}
```

# Persistent Bugger. [6 kyu] #130

```js
function persistence(num) {
  //code me
let count = 0;
  let result = 1;
  let arrayNum = num
    .toString()
    .split("")
    .map((n) => Number(n));
  console.log("array avant boucle : ", arrayNum);
  if (num.toString().length == 1) return 0;

  do {
    for (let i = 0; i < arrayNum.length; i++) {
      result *= arrayNum[i];
      console.log("result for : ", arrayNum[i]);
    }
    count++;
    if (result.toString().length == 1) break;
    arrayNum.splice(0, arrayNum.length);
    arrayNum = result
      .toString()
      .split("")
      .map((n) => Number(n));
    console.log("new arrayNum : ", arrayNum);
    result = 1;
  } while (true);
  return count;
}
```

# The highest profit wins! [7 kyu] #131

```js
function minMax(arr) {
  let min = arr[0];
  let max = arr[0];
  for (let i = 0; i < arr.length; i++) {
    min = min < arr[i] ? arr[i] : min;
    max = max > arr[i] ? arr[i] : max;
  }
  const newArr = [];
  newArr.splice(0, 0, max, min);
  return newArr;
}
```

# Bouncing Balls [6 kyu] #132

```js
function bouncingBall(h, bounce, window) {
  let c = 0;
  let isFalling = true;
  if (h <= window || bounce >= 1 || bounce <= 0) return -1;
  do {
    if (!isFalling) {
      h = h * bounce;
    }
    c += h > window ? 1 : 0;
    isFalling = !isFalling;
  } while (h > window);
  return c;
}
```

# Square Every Digit [7 kyu] #133

```js
function squareDigits(num) {
  return Number(
    num
      .toString()
      .split("")
      .map((x) => x * x)
      .join("")
  );
}
```

# Grasshopper - Personalized Message [8 kyu] #134

```js
function greet (name, owner) {
  return name == owner ? "Hello boss" : "Hello guest";
}
```

# DNA to RNA Conversion [8 kyu] #135

```js

function DNAtoRNA(dna) {
  return dna.replace(/[T]/g, "U");
}

```

# Find the odd int [6 kyu] #136

```js

function findOdd(A) {
  return A.find(
    (x) =>
A.reduce((a, n) => {
        a[n] = (a[n] || 0) + 1;
        return a;
      }, {})[x] % 2
  );
}
```

# Reversed sequence [8 kyu] #137

```js
const reverseSeq = (n) => {
  const newArray = [];
  for (let i = 0; i < n; i++) {
    newArray.push(n - i);
  }
  return newArray;
};
```

# Reversed Strings [8 kyu] #138

```js
function solution(str){
    return str.split("").reverse().join("");
}
```

# Convert a string to an array [8 kyu] #139

```js
function stringToArray(string){

  return string.split(" ");

}
```

# Sum without highest and lowest number [8 kyu] #140

```js
function sumArray(array) {
  if (!Array.isArray(array)) return 0;
  return array
    .sort((a, b) => b - a)
    .slice(1, -1)
    .reduce((a, c) => a + c, 0);
}
```

# Grasshopper - Summation [8 kyu] #141

```js
var summation = function (num) {
  let res = num;
  if (!num) return false;
  return res + summation(num-1);
}
```

# Return Negative [8 kyu] #142

```js
function makeNegative(num) {
  return num < 0 ? num : -num;
}
```

# Abbreviate a Two Word Name [8 kyu] #143

```js

function abbrevName(name) {
  return name.match(/\b[a-zA-Z]/g).join(".").toUpperCase();
}
```

# Remove exclamation marks [8 kyu] #144

```js
function removeExclamationMarks(s) {
  return s.split("").filter(l => l !== "!").join("");
}
```

# Remove First and Last Character [8 kyu] #145

```js
function removeChar(str) {
  return str
    .split("")
    .filter((l, i) => i !== 0)
    .filter((l, i) => i < str.length - 2)
  .join("");
}
```

# Replace With Alphabet Position [6 kyu] #146

```js
function alphabetPosition(text) {
  return text
    .toLowerCase()
    .replace(/[^a-zA-Z]/g, "")
    .split("")
    .map((char) => char.charCodeAt(0) - 96)
    .join(" ");
}
```

# Array.diff [6 kyu] #147

```js

function arrayDiff(a, b) {
  console.log(a.filter((x) => x == 1));
  return a.filter((x) => b.find((y) => y == x) !== x);
}
```

# Beginner Series #3 Sum of Numbers [7 kyu] #148

```js
function getSum(a, b)
{
  if ( a == b ) return a;
  let start = a > b ? b : a;
  const end = a > b ? a : b;
  let sum = 0;
  do {
    sum += start;
    start++;
  } while (start < end + 1)
  return sum;
}
```

# Sum of the first nth term of Series [7 kyu] #149

```js
function SeriesSum(n) {
  let r = 0;
  for (let i = 0; i < n; i++) {
    r += i ? 1 / (i * 3 + 1) : 1;
  }
  return String(r.toFixed(2));
}
```

# Playing with digits [6 kyu] #150

```js

function digPow(n, p) {
  const digits = n.toString().split("").map(Number);
  let result = 0;
  let pCounter = p;
  for (let i = 0; i < digits.length; i++) {
    result += Math.pow(digits[i], pCounter++);
  }
  if (Number.isInteger(result / n)) return result / n;

  return -1;
}
```

# Categorize New Member [7 kyu] #151

```js
function openOrSenior(data){
  strArray = [];
  for (let i = 0 ; i < data.length ; i++) {
    if (data[i][0] > 54 && data[i][1] > 7) strArray.push("Senior");
    else strArray.push("Open");
  }
  return strArray;
}
```

# If you can't sleep, just count sheep!! [8 kyu] #152

```js
var countSheep = function (num){
  let str = ""
for (let i = 1 ; i < num + 1 ; i++)  {
    str += `${i} sheep...`;
  }
  return str;
}
```

# A Needle in the Haystack [8 kyu] #153

```js
function findNeedle(haystack) {
  return `found the needle at position ${haystack.findIndex((word, index) => {
    if (word == "needle") return true;
  })}`;
}
```

# Invert values [8 kyu] #154

```js
function invert(array) {
   return array.map((x) => -x)
}
```

# Rock Paper Scissors! [8 kyu] #155

```js
const rps = (p1, p2) => {
  if (p1 === p2) return "Draw!";
  if (p1 == "rock") {
    switch (p2) {
        case "scissors":
          return "Player 1 won!"
case "paper":
          return "Player 2 won!"
default:
          break;
    }
  }
  if (p1 == "paper") {
    switch (p2) {
        case "rock":
          return "Player 1 won!"
case "scissors":
          return "Player 2 won!"
default:
          break;
    }
  }
  if (p1 == "scissors") {
    switch (p2) {
        case "rock":
          return "Player 2 won!"
case "paper":
          return "Player 1 won!"
default:
          break;
    }
  }
};
```

# Delete occurrences of an element if it occurs more than n times [6 kyu] #156

```js
function deleteNth(arr, n) {
  const counts = {};
  return arr.filter((x) => {
    console.log(counts);

    return (counts[x] = (counts[x] || 0) + 1) <= n;
  });
}
```

# Who likes it? [6 kyu] #157

```js
function likes(names) {
  switch (names.length) {
    case 0:
      return "no one likes this";
    case 1:
      return `${names[0]} likes this`;
    case 2:
      return `${names[0]} and ${names[1]} like this`;
    case 3:
      return `${names[0]}, ${names[1]} and ${names[2]} like this`;
    default:
      return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
  }
}
```

# Returning Strings [8 kyu] #158

```js
function greet(name){
  //your code here
return `Hello, ${name} how are you doing today?`
}
```

# Reverse the bits in an integer [7 kyu] #159

```js

function reverseBits(n) {
  const nBits = n.toString(2);
  const nReversed = nBits.toString().split("").reverse().join("");
  const integer = parseInt(nReversed, 2);
  return integer;
}
```

# Counting Duplicates [6 kyu] #160

```js
function duplicateCount(text) {
  const counter = {};
  for (char of text) {
    if (char.toLowerCase() in counter) {
      counter[char.toLowerCase()] += 1;
    } else {
      counter[char.toLowerCase()] = 1;
    }
    if (!text.length) return 0;
  }
  console.log(counter);
  let maxValue = 2;
  let numberMaxValue = 0;
  for (value in counter) {
    console.log("value : ", counter[value]);
    numberMaxValue += counter[value] > 1 ? 1 : 0;
    if (maxValue < counter[value]) {
      maxValue = counter[value];
      numberMaxValue = 1;
    }
  }
  console.log(numberMaxValue);
  return numberMaxValue;
}
```

# ROT13 [5 kyu] #161

```js
function rot13(str) {
  return str.replace(/[a-zA-Z]/g, (char) => {
    const base = char <= "Z" ? 65 : 97; //65 pour 'A', 97 pour 'a'
return String.fromCharCode(((char.charCodeAt(0) - base + 13) % 26) + base);
  });
}
```

# Simple Pig Latin [5 kyu] #162

```js
function pigIt(str) {
  return str.replace(
    /\b(\w)(\w*)\b/g,
    (match, firstLetter, restOfWord) => `${restOfWord}${firstLetter}ay`
  );
}
```

# Duplicate Encoder [6 kyu] #163

```js
function duplicateEncode(word) {
  const counter = {};
  let str = "";
  for (const char of word) {
    if (char.toLowerCase() in counter) {
      counter[char.toLowerCase()] += 1;
    } else {
      counter[char.toLowerCase()] = 1;
    }
  }
  return word
    .split("")
    .map((letter) => {
      if (counter[letter.toLowerCase()] > 1) return ")";
      else return "(";
    })
    .join("");
}
```

# Maximum subarray sum [5 kyu] #164

```js
var maxSequence = function (arr) {
  let maxSum = 0;
  let tempSum = 0;
  for (const numb of arr) {
    tempSum += numb;
    if (tempSum < 0) tempSum = 0;
    maxSum = maxSum < tempSum ? tempSum : maxSum;
  }
  return maxSum;
};
```

# Convert string to camel case [6 kyu] #165

```js

function toCamelCase(str) {
  return str.replace(/([-_][a-zA-Z])/g, (match) => {
    return match[1].toUpperCase();
  });
}
```

# Complementary DNA [7 kyu] #166

```js
function dnaStrand(dna) {
  return dna.replace(/A|T|G|C/g, (char) => {
    switch (char) {
      case "A":
        return "T";
      case "T":
        return "A";
      case "G":
        return "C";
      case "C":
        return "G";
    }
  });
}
```

# Sentence Smash [8 kyu] #167

```js
function smash (words) {
   return words.join(" ");
};
```

# Disemvowel Trolls [7 kyu] #168

```js
function disemvowel(str) {
  return str.replace(/[aeiou]/gi, "");
}
```

# Get the Middle Character [7 kyu] #169

```js
function getMiddle(s) {
  const sArray = s.split("");
  console.log(sArray);
  const middleArray = sArray.length / 2;
  const isPair = sArray.length % 2 ? false : true;
  console.log(middleArray);
  //   console.log("test : ", sArray.splice(2, 2));
return isPair
? sArray.splice(middleArray - 1, 2).join("")
    : sArray.splice(Math.floor(middleArray), 1).join("");
}
```

