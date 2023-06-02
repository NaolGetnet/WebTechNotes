# 30 days of JS notes

---

## Day 1

- Unassigned variables are undefined.
- The name of a variable can only include $ and _ from the special characters.

## Day 2

### Data types

- Primitive (unchangeble)
- Non-primitive (changable)

### Non-Primitive

- Objects and arrays
- not comparable

### Primitive

- Numbers, String, Booleans, Null, Symbol, Undefined

Number

- `Math.`

String

- Many methods like split(), toLower(), toUpper(), trim(’specified text’)
- \n: new line
- \t: Tab, means 8 spaces
- \\: Back slash
- \': Single quote (')
- \": Double quote (")

### Casting

- String to Float   `parseFloat`
- String to Int   `parseInt`
- Float to Int   `parseInt`

## Day 3

Boolean

### Truthy values

- All numbers(positive and negative) are truthy except zero
- All strings are truthy except an empty string ('')
- The boolean true

### Falsy values

- 0
- 0n
- null
- undefined
- NaN
- the boolean false
- '', "", ``, empty string

Ternary operators

```
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

Window operators

- alert(’wow’);
- let num = prompt( ’now’, optional)
- `const agree = confirm('Are you sure you like to delete? ')`

Date Objects

- Many…

`const now = new Date()`

`console.log(now.getHours())`

`console.log(now.getMinutes())`

## Day 4

- If
- If else
- If else if else
- ternary
- switch

## Day 5

Array

- Methods to create an array

```
let companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'
const companies = companiesString.split(',')

console.log(companies) // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"]
```

```
const eightXvalues = Array(8).fill('X') // it creates eight element values filled with 'X'
console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']
 
Array(8) alone makes eight empyies
```

- Concatination

`const thirdList = firstList.concat(secondList)`

- length

```
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.length) // -> 5 is the size of the array
```

- pop()
- push()
- indexOf (’ banana ‘)
- lastindexOf (’ banana ‘)
- [Array.is](http://Array.is)Array()
- toString()
- join( “, ”)
- slice(0,5)
- reverse()
- sort()
- shift()
- unshift()

## Day 6

Loops types

- for
- while
- 
- 
- for of

```
const numbers = [1, 2, 3, 4, 5]
const newArr = []
let sum = 0

for (const num of numbers) {
  newArr.push( num ** 2)
}

// [1, 4, 9, 16, 25]

for (const num of numbers) {
  console.log(num * num)
}

// 1 4 9 16 25
```

### 

## **Day 7**

Types of **Functions**

- Unlimited parameter function

```
function sumAllNums() {
  let sum = 0
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i]
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4)) // 10
```

- Anonymous

```
const anonymousFun = function() {
  console.log(
    'I am an anonymous function and my value is stored in anonymousFun'
  )
}
```

- **Expression Function**

```
// Function expression
const square = function(n) {
  return n * n
}

console.log(square(2)) // -> 4
```

- Self-invoking Functions

anonymous functions which do not need to be called to return a value.

```
(function(n) {
  console.log(n * n)
})(2) // 4, but instead of just printing if we want to return and store the data, we do as shown below

let squaredNum = (function(n) {
  return n * n
})(10)

console.log(squaredNum)
```

### Arrow Functions

```
const square = n => {
  return n * n
}

console.log(square(2))  // -> 4

// if we have only one line in the code block, it can be written as follows, explicit return
const square = n => n * n  // -> 4
```

```
const changeToUpperCase = arr => {
  const newArr = []
  for (const element of arr) {
    newArr.push(element.toUpperCase())
  }
  return newArr
}

const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
console.log(changeToUpperCase(countries))

// ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
```

```
const printFullName = (firstName, lastName) => {
  return `${firstName} ${lastName}`
}

console.log(printFullName('Asabeneh', 'Yetayeh'))
```

The above function has only the return statement, therefore, we can explicitly return it as follows.

`const printFullName = (firstName, lastName) => `${firstName} ${lastName}`

console.log(printFullName('Asabeneh', 'Yetayeh'))`

## Day 8

### Scope

- var works in the entire function
- const and let work in the blocks
- recommended to use let and const
- if we change it in a block it is changed relatively globally

### Object

- is a key value pair
- The value of properties or keys could be a string, number, boolean, an object, null, undefined or a function.

```
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js'
  ],
  isMarried: true
}
console.log(person)
```