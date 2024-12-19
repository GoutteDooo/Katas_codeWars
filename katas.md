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

