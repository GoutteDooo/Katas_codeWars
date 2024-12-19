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

