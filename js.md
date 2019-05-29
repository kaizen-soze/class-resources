# Intro to Javascript
Javascript (or ECMAScript) is a programming language that adds interactivity to web sites.

## Variables

A variable is a reference to a space in a computer's memory that contains a specific piece of information. Since humans are not good at referencing memory addresses, we give them human-readable names.

Variable names should be camelCase.

Camel Case (technically, lower camel case) is where you combine words and remove spaces. Each new word gets a capital letter.

Examples:

* valueMeal
* myLittlePony
* iJustSavedABunchOfMoneyOnMyCarInsurance

Naming things can be hard, so try to come up with names that are descriptive of what the variable is going to be used for.

Variables can be immutable or mutable. Immutable variables can't be changed. Mutable variables can.

To define an immutable variable, use the `const` keyword. To define a mutable variable, use the `let` keyword.

Typically you should use `const` when defining a variable. If you realize that you need to allow the value in the variable to change, use the `let` keyword.

```
// Names rarely change
const firstName = 'Ben'

// Subtotals will probably change often
let subtotal = 9.27
subtotal = 10.32
```

## Data Types
Variables can be one of several different data types.

### Strings
A string is just text. Strings must always be surrounded with a single quote.

```
const firstName = 'John'
const lastName = 'Doe'
const pi = '3.14159'
```

### Integers
Integers are whole numbers.

```
const oneHundred = 100
const age = 44
const negativeValue = -10
```

### Floating Point Numbers
Floating point numbers are numbers that have a decimal in them. Javascript doesn't care if you're referring to currency or scientific notation; if it has a decimal it's a floating point number. This type of number is also referred to as a float.

```
const pi = 3.14159
const total = 13.94
const taxRate = 0.0725
const age = 13.0
```

### Boolean Values
A boolean value is either `true` or `false`.

`true` and `false` are keywords in javascript that have special meaning. If a value is `true`, it represents a positive result. If a value is `false`, it represents a negative result.

```
const booleanValue = true
const resultIsFalse = false
```

One fun, but kind of confusing, fact about booleans is that the numeric values `1` and `0` can also be read as boolean values. We'll talk about this more when we discuss `if` statements.

### Null values
A null value represents nothing. It's not `true`. It's not `false`. It literally has no value at all.

```
let myVariable = null
// ...later
myVariable = 16
```

### Arrays
An array is a collection of information. This collection doesn't have to be unique. The elements in the collection can be any type of value, but typically an array is full of the same kind of data.

```
const fibonacci = [1, 2, 3, 5, 8, 13, 21]
const students = ['Cara', 'Mia', 'Jack']
```

### Objects
Objects are also collections of information, but they have more built-in capabilities than arrays. We'll cover objects more in-depth later.

## Mathematical Operations
It's common to perform mathematical operations inside code. By and large you'll use the operators you're already familiar with.

### Addition
Use the `+` symbol to perform addition.

```
const eight = 5 + 3
const nine = eight + 1
cont seventeen = eight + nine
```

### Subtraction
Use the `-` symbol to perform subtraction

```
const two = 5 - 3
```

### Multiplication
Use the `*` symbol to perform multiplication.

```
const seventyTwo = 8 * 9
```

### Division
Use the `/` symbol to perform division

```
const four = 32 / 8
```

### Exponent
Use the `**` symbol to perform exponential operations

```
const twentySeven = 3 ** 3
const nine = 3 ** 2
```

### Modulus
Use the `%` symbol to find the modulus. The easiest way to think of a modulus is the remainder that's left after doing division.

```
const one = 16 % 5          // returns 1
const oneAgain = 221 % 2    // returns 1
const zero = 12 % 4         // returns 0
```

When you divide 16 by 5, it goes into 16 evenly 3 times and you are left with a 1...so output of `16 % 5` is `1`.

When you divide 12 by 4, it goes into 12 evenly and there is nothing left over, so the output of `12 % 4` is 0.

### Order of Operations
The Order of Operations is the order in which the computer will perform calculations.

The order is:

1. Exponentiation
2. Multiplication
3. Division
4. Modulus
5. Addition
6. Subtraction

## Console

The javascript console is a tool for developers to interact with JavaScript from within the web browser.

Writing messages to the console is easy.

```
console.log('Hello, World!')
console.log(12 + 2)
```

To open the console:

Chrome on Mac: COMMAND + OPTION + J
Chrome on Windows: CTRL + SHIFT + J

## Comparison Operators

### Less Than
The `<` operator checks to see if the value on the left is less than the value on the right. It returns true or false, based on the outcome.

```
5 < 10    // returns true
5 < 2     // returns false
```

### Greater Than
The `>` operator checks to see if the value on the left is greater than the value on the right.

```
5 > 10    // returns false
5 > 2     // returns true
```

### Less Than or Equal To
The `<=` operator checks to see if the value on the left is less than or equal to the value on the right.

```
5 <= 10    // returns true
5 <= 2     // returns false
5 <= 5     // returns true
```

### Greater Than or Equal To
The `>=` operator checks to see if the value on the left is greater than or equal to the value on the right.

```
5 >= 10    // returns false
5 >= 2     // returns true
5 >= 5     // returns true
```

### Loose Equality

The `==` operator checks to see if the value on the left is equal to the value on the right. It doesn't care if you're comparing strings to numbers, it will check for the meaning of what is passed.

```
let myNumber = "5"
myNumber == 5    // returns true

myNumber = 6
myNumber == 6   // returns true

myNumber = "eight"
myNumber == 8   // returns false because you
                // compared a string to a number

let name = 'Ben';
name == 'Ben'     // returns true

const name = 'Ben '
name == 'Ben'     // returns false due to extra space

const name 'ben'
name == 'Ben'     // returns false due to case mismatch
```

### Strict Equality

The `===` operator checks to see if the value on the left is equal to the value on the right. It **also** checks to see if the **type** of each value is the same. If you compare a string and a number, it will fail...even if loose equality says it's the same.

```
let myNumber = "5"
myNumber === 5    // returns false

myNumber = 6
myNumber === 6   // returns true

let myNumber = "eight"
myNumber === 8   // returns false

let name = 'Ben';
name === 'Ben'     // returns true

const name = 'Ben '
name === 'Ben'     // returns false due to extra space

const name 'ben'
name === 'Ben'     // returns false due to case mismatch
```

### Loose Inequality

The `!=` operator checks to see if the value on the left is not equal to the value on the right. It doesn't care if you're comparing strings to numbers, it will check for the meaning of what is passed.

```
let myNumber = "5"
myNumber != 5    // returns false

myNumber = 6
myNumber != 6   // returns false

myNumber = "eight"
myNumber != 8   // returns true because you
                // compared a string to a number

let name = 'Ben';
name != 'Ben'     // returns false

const name = 'Ben '
name != 'Ben'     // returns true due to extra space

const name 'ben'
name != 'Ben'     // returns true due to case mismatch
```

### Strict Inequality

The `!==` operator checks to see if the value on the left is not equal to the value on the right. It **also** checks to see if the **type** of each value is not same.

```
let myNumber = "5"
myNumber !== 5    // returns true because the types do not match

myNumber = 6
myNumber !== 6   // returns false

myNumber = "eight"
myNumber !== 8   // returns true because you
                 // compared a string to a number, so
                 // the types don't match

let name = 'Ben';
name !== 'Ben'     // returns false

const name = 'Ben '
name !== 'Ben'     // returns true due to extra space

const name 'ben'
name !== 'Ben'     // returns true due to case mismatch
```

## Logical Operators
Logical operators allow you to chain comparisons.

### `&&` Operator
The `&&` operator evaluates to true if the conditions on each side of the operator are true. When we refer to this operator we call it the AND operator.

```
const likesCats = true
const likesDogs = true
const likesIguanas = true

// Evaluates to true
const likesPets = likesCats && likesDogs

// Evaluates to true
const likesAllPets = likesCats && likesDogs && likesIguanas
```

### `||` Operator
The `||` operator evaluates to true if the conditions on one side of the operator is true. When we refer to this operator we call it the OR operator.

```
const likesCats = true
const likesDogs = false
const likesIguanas = true


// Evaluates to true
const likesPets = likesCats || likesDogs

// Evaluates to true
const likesAllPets = likesCats || likesDogs || likesIguanas
```

### `!` Operator
Place the `!` operator in front of a condition that evaluates to false and you will get a response of true.

If you place this in front of a condition that evaluates to true, it will return false.

We call this the NOT operator.

```
const water = 'H2O'
const peroxide = 'H2O2'

// Evaluates to true
const notWater = !(water === peroxide)
```

Humans have a difficult time thinking in negative terms. You're not going to need this operator very often, but when you do it can be useful. Usually the NOT operator can be avoided by restructuring your code.

## Conditional Logic

Conditional logic is used to direct the flow of the program based on the outcome of logical tests.

### `if` Statement
The most common type of conditional logic used is the `if` statement.

```
if (condition is true) {
    // Do a thing
}
```

Conditional logic uses comparison operators (`<`, `>`, `!=`, etc) to execute code if the logic is true.

```
const age = 20
if (age < 21) {
    console.log('You must be 21 or older to proceed.')
}

const votingAge = 18
if (votingAge >= 18) {
    console.log('You are eligible to vote!')
}
```

### `else` Statement
An `else` statement executes if the conditional in the `if` statement evaluates to false.

```
if (condition is true) {
    // Do a thing
} else {
    // Do a different thing
}
```

This allows you to take action if the thing you are testing for is not true.

```
const age = 20
if (age < 21) {
    console.log('You must be 21 or older to proceed.')
} else {
    console.log('You have passed the age check!')
}

const votingAge = 18
if (votingAge >= 18) {
    console.log('You are eligible to vote!')
} else {
    console.log('You must be 18 or older in order to vote')
}
```

### `else if` Statement

The `else if` statement allows you to test for a different scenario if you want to take action based on more than two situations.

```
if (condition is true) {
    // Do a thing
} else if (a second condition is true) {
    // Do a different thing. Executes if block one is
    // false and block two is true.
} else {
    // Do a third thing if both other blocks are true.
}
```

`Else if` statements are not limited to three blocks. You can chain `else if` statements for as long as necessary. The problem with this is that as the blocks get longer, the easier it is to avoid logic errors.

```
const name = 'Jonathan'
if (name == 'Jack') {
    console.log('You are on the Programming Pandas team!')
} else if (name == 'Jonathan') {
    console.log('You are on the Programming Pandas team!')
} else if (name == 'Mia') {
    console.log('You are on the Programming Pandas team!')
} else {
    console.log('You are on the Codeasauras Rex team!')
}
```

### Switch operator

An easier way to avoid lengthy if/else if blocks is to use the switch operator. The switch operator lets you test multiple conditionals in a more concise manner than if/else.

```
switch(conditional statement) {
  case x:
    // Do a thing
    break;  // Break out of this switch statement
  case y:
    // Do another thing
    break;
  default:
    // If nothing matches, do this
}
```