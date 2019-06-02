# Javascript Arrays
This file doesn't contain everything there is to know about arrays and their associated methods. For more info, check out the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

## Basics

An array is a numerically-indexed collection of javascript objects. While an array can contain a wide number of different variables, in practice an array typically contains the same type of element.

```
const animals = ['cat', 'dog', 'rabbit', 'ferret', 'squirrel']
const numbers = [12, 24, 316, 86, 130]
```

You can access individual elements of an array by referring to their index.

```
// Outputs: dog
console.log(animals[1])

// Outputs: 86
console.log(numbers[3])
```

The number of elements in an array can be accessed via the `length` property.

```
// Outputs: 5
console.log(animals.length)
```

## Common Array Functions

### Add a new item to the end of an array
To add an item to the end of an array, use the [`push()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push).


```
const animals = ['cat', 'dog', 'rabbit', 'ferret', 'squirrel']

// Adds 'mouse' after 'squirrel'
animals.push('mouse')

// It's possible to add multiple items at once
animals.push('elephant', 'tiger')
```

### Add a new item to the beginning of an array
The [`unshift()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift) allows you to add a new item to the front of an array.

```
const animals = ['cat', 'dog', 'rabbit', 'ferret', 'squirrel']

// Adds 'mouse' before 'cat'
animals.unshift('mouse')

// It's possible to add multiple items at once
animals.unshift('elephant', 'tiger')

// Output: ['elephant', 'tiger', 'mouse', 'cat', 'dog', 'rabbit', 'ferret', 'squirrel']
console.log(animals)
```

### Remove an item from the end of an array
Use the [`pop()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) to remove an item from the end of an array.

```
const beatles = ['John', 'Paul', 'George', 'Ringo']
const last = beatles.pop()

// Outputs: ['John', 'Paul', 'George']
console.log(beatles)

// Outputs: 'Ringo'
console.log(last)
```

### Remove an item from the beginning of the array
The [`shift()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift) removes the first item from the beginning of an array.

```
const beatles = ['John', 'Paul', 'George', 'Ringo']
const first = beatles.shift()

// Outputs: ['Paul', 'George', 'Ringo']
console.log(beatles)

// Outputs: 'John'
console.log(first)
```

### Reverse the order

The aptly-named [`reverse()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse) reverses the order of elements in an array.

```
const numbers = [1, 2, 3, 4, 5]
numbers.reverse()

// Outputs: [5, 4, 3, 2, 1]
console.log(numbers)

const animals = ['cat', 'dog', 'rabbit', 'ferret', 'squirrel']
animals.sort()

// Outputs: ['squirrel', 'ferret', 'rabbit', 'dog', 'cat']
console.log(animals)
```

### Sort an array
When the order of elements matters, you can use the [`sort()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort).

```
const numbers = [8, 39, 302, 84, 22]
numbers.sort()

// Outputs: [8, 22, 39, 84, 302]
console.log(numbers)

const animals = ['cat', 'dog', 'rabbit', 'ferret', 'squirrel']
animals.sort()

// Outputs: ['cat', 'dog', 'ferret', 'rabbit', 'squirrel']
console.log(animals)
```
> Note: It's possible to pass a custom sorting function to the sort() function so that things are sorted in the precise way you want. Check the documentation for more info

### Join arrays to one another
To concatenate arrays, use the [`concat()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat).

```
const data1 = ['one', 'two']
const data2 = ['three', 'four']
const data3 = ['five','six']

const joined = data1.concat(data2, data3)

// Outputs: ['one', 'two', 'three', 'four', 'five', 'six']
console.log(joined)
```

### Check if a value exists in the array
The [`includes()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) allows you to check for the existence of a specific value in an array. It doesn't do partial matches; either the value is found or it is not.

```
const names = ['Arya', 'Bran', 'Jon', 'Sansa']

// Outputs: true
console.log(names.includes('Sansa'))

// Outputs: false
console.log(names.includes('ran'))
```

### Find first occurence of an entry
The [`indexOf()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf) returns the first index that matches the value you're searching for. If the value can appear multiple times, you'll only see the first result. If no match is found, the method returns `-1`

```
const names = ['Arya', 'Bran', 'Jon', 'Sansa']

if (names.indexOf('Tyrion') !== -1) {
    console.log('Tyrion found as a name in the array')
} else {
    console.log('Tyrion not found!')
}
```

### Remove part of an array
The [`slice()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) removes part of an array and returns it to another variable. The original array isn't modified. 

```
const names = ['Britney', 'Avril', 'Miley', 'Katy', 'Carly']
const lastTwo = names.slice(3)

// Output: ['Katy', 'Carly']
console.log(lastTwo)

// Output: ['Avril', 'Miley']
console.log(names.slice(1, 3))
// We start at index 1, 'Avril', and stop on the third item after we begin, which is 'Katy'. The method returns two values.
```

### Perform an action on each item in the array
Instead of using a loop, we can use the [`forEach()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) to do something for each item in an array.

```
const music = ['piano', 'drums', 'guitar', 'bass']

music.forEach(function(item){
    console.log(`Do you play the ${item}?`)
})

const numbers = [2, 4, 6, 8, 10]

numbers.forEach(function(element){
    const square = element ** element
    console.log(`The square of ${element} is ${square}`)
})
```
> Note: There is no way to stop processing an array once you begin using `forEach()`, so if you only want to process some elements, this is not the right method for that.



