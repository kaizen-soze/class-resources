# Javascript Numbers
This file doesn't contain everything there is to know about numbers and their associated methods. For more info, check out the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number).

## Basics

Numbers are fairly easy to create.

```
// Most of the time all you need is to define your number.
const myNumber = 42
const floatingPoint = 98.6

// If you really want to, you can use the Number method.
const otherNumber = new Number('100')

// Returns a value of `NaN`, which stands for "Not a Number"
const notANumber = new Number('This is not a number')
```

Once a number is created, Javascript recognizes it as a number object and gives it access to a lot of different functions. 

## Common Number Functions

### Check if a number is an integer
There will be times where you'll receive a number of some sort but you won't know immediately if you're working with an integer or a floating point number. To check if it's a whole number, use the [`isInteger()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isInteger).

```
let x = 15

// Returns true
console.log(x.isInteger())

x = 15.0
// Returns true
console.log(x.isInteger())

x = 15.00001
// Returns false
console.log(x.isInteger())

```

### Rounding a number to the nearest decimal point
The [`toFixed()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed) allows you to round a number to a specified number of decimal places.

```
const i = 9.52387

// Outputs: 9.52
console.log(i.toFixed(2))
```
