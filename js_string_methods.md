# Javascript Strings
This file doesn't contain everything there is to know about strings. For more info, check out the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String).

The true utility of most of these methods is when you combine them with each other; you can do some really powerful things.

## Basics

A string literal can be built in several ways.

```
// Most of the time all you need is a single quote surrounding
// your string
let myString = 'This is a string!'

// Notice the double quotes
myString = "I'm using an apostrophe!"
myString = 'It\'s also possible to use apostrophes like so'

let templateLiteral = `This is a template literal`

templateLiteral = `It uses backticks to 
contain a string. The text will be rendered
as-is, line breaks included.`

const myVar = 'variables'
templateLiteral = `A template literal can include other ${myVar}
or HTML markup<br />`

const appendStrings = 'You can join strings ' +
                    'by using the + symbol'

const backslash = 'You can also use backslashes \
to indicate that there should be a line break in a string'

const noOneDoesThis = new String('This is a string!')
```

Once a string is created, Javascript recognizes it as a string object and gives it access to a lot of different functions. These functions can be used to manipulate the strings in various ways.

You can check the length of a string with the `.length` property.

```
const name = 'Tabitha'
// Prints 7
console.log(name.length)
```

## Common String Functions

### Access a specific character
There are two methods for accessing the individual elements of a string.

```
const name = 'Tabitha'

// Both of these output the letter 'b'
console.log(name.charAt(2))
console.log(name[2])
```

The most common method by far is bracket-style.

### Join two strings
There are two methods to concatenate strings; the plus operator and the [`concat()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/concat).

```
const seq1 = 'xylo'
const seq2 = 'phone'

const seq3 = seq1 + seq2

// Returns 'xylophonexylophone`
const seq4 = seq1.concat(seq2, seq3)
```

### Check if a substring exists
It's very common to search for the existence of a string inside of another string. We can use the [`includes()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes) to check for the existince of a target string.

```
const target = 'script'

// returns true
const targetExists = 'unscripted'.includes(target)
```

### Finding where a character is
Another common task is finding where in a string a character or sequence begins. For this we use the [`indexOf()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf).

```
const message = 'My phone number is (352) 555-1212'
const phoneStart = message.indexOf('(')
```

### Replace a string with another string
It's possible to substitute a set of characters with another set of characters. This is done with the [`replace()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace).


```
const newPet = 'falcon'
const oldPet = 'cat'

const statement = 'My favorite animal is the cat'

console.log(statement.replace(oldPet, newPet))
```

> Note: The `replace()` method is much more complex than this example makes it appear. When using this method to replace characters, only the first match is replaced. There is a way to replace all occurrences in a string, but it uses regular expressions, which is beyond our scope.

### Create a substring
The [`slice()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice) allows us to extract a specific sequence of characters.

```
const toxic = "I'm addicted to you, don't you know that you're toxic?"

// outputs: that you're toxic?
console.log(toxic.slice(36))

// outputs: addicted to you
console.log(toxic.slice(4, 19))

// outputs: you're toxic?
console.log(toxic.slice(-13)) 

// outputs: you're to
console.log(toxic.slice(-13, -4))
```

> Note: The `substring()` method also exists, but doesn't have as many options for use.

### Split a string
The [`split()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split) turns a string into an array of strings that are separated by the character or sequence you specify.

```
const toxic = "I'm addicted to you, don't you know that you're toxic?"

const words = toxic.split(' )

// outputs: addicted
console.log(words[1])

const phoneNumber = '352.555.1212'
const parts = phoneNumber.split('.')
const areaCode = parts[0]

// outputs: 352
console.log(areaCode)
```

### Change case
To change the case of an entire string, use the [`toUpperCase()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase) and [`toLowerCase()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase).

```
const normalCase = "I'm not shouting, am I?"
const upperCase = normalCase.toUpperCase()
const lowercase = normalCase.toLowerCase()

// Output: I'M NOT SHOUTING, AM I?
console.log(upperCase)

// Output: i'm not shouting, am i?
console.log(lowerCase)
```

### Remove whitespace from the ends of a string
When you are interacting with user input, it's common to run into extra whitespace; people love using the space bar. The [`trim()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/trim) removes whitespace from the beginning and end of a string.

```
const userAge = `


94


    
`.trim()

// Output: 94
console.log(userAge)
```
