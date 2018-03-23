# JavaScript Overview - Codecademy

### Console is a tool used to record the output of the JS programs.
  ```console.log("Hello!");```

#### 4 primitive data types:
  1. **Strings** (any grouping of keyword characters, with quotes '' or double quotes "")
  2. **Numbers** (any numbers, including decimals)
  3. **Booleans** (true or false)
  4. **Nulls** (only null, it represents absence of a value
  5. **Undefined** (JS assigns the undefined data type to variables that are not assigned a value.)

#### Math operators:
  1. Add: +
  2. Subtract: -
  3. Multiply: *
  4. Divide: /

#### Properties:
When I introduce a new piece of data into a JavaScript program, the browser saves it as an instance of the data type.
An instance is an individual case (or object) of a data type.

  For example: JS will save a new piece of data 'Hello' as a string instance in the computer's memory.
  Another example: Number 40.7 is stored as an instance of the number data type.
  An instance, like the string 'Hello' has an additional information attached to it - property.

  Example: .length property shows the number of characters in a string
  Example: ```console.log('Word'.length)``` -> the output is 4

#### Bult-in methods:
  Length of a string is calculated when an instance is created, but string instance also has methods that calculate new information as needed.
  Built-in methods are called on an instance, they perform actions that generate an output.

[JS introduction in Polish - link](https://developer.mozilla.org/pl/docs/Web/JavaScript/Wprowadzenie_do_programowania_obiektowego_w_jezyku_JavaScript)<br>
[JS methods in English - link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype)


Instance methods require an instance before you use them.

#### Variables:
Variables allow us to assign data to a word and use the word to reference the data
##### 2 ways to declare variables:
  1. **let** (can be reassigned)
  2. **const** (*constant variable*), creates a new variable with value that cannot change

### Mathematical Assignement Operators
**+=, -=, *=** - perform mathematical operation of the first operator<br>
**++, --** - increment and decrement operators, increasing or decreasing a number of variable by one, respectively.

### Methods
`.toUpperCase()`<br>
`.startsWith()` <br>

`console.log('Hello'.toUpperCase());` // 'HELLO'
`console.log('Hey'.startsWith('H'));` // true

`Math.random()`: returns random number between 0 and 1<br>
`Math.random() * 50`: returns random number between 0 and 50<br>
`Math.Floor()`: takes the decimal number and rounds down to the nearest whole number<br>
`Math.ceil()`: returns smallest integer greater than or equal to a given<br>

`console.log(Math.random());` // random number between 0 and 1

### String interpolation <br>
let myPet = 'armadillo'; <br>
console.log('I own a pet ' + myPet + '.');<br>
// Output: 'I own a pet armadillo.'

## String interpolation II
used in JS (ES6)

let myPet = 'dog'; <br>
console.log(`I own a pet ${myPet}.`); <br>
let myName = 'Patka'; <br>
let myCity = 'Poznan'; <br>
console.log(`My name is ${myName}. My favorite city is ${myCity}.`); <br>

### Variables review
 - Variables hold reusable data in a program.
 - JavaScript will throw an error if you try to reassign const variables.
 - You can reassign variables that you create with the let keyword.
 - Unset variables store the primitive data type undefined.
 - Mathematical assignment operators make it easy to calculate a new value and assign it to the same variable.
 - The + operator is used to interpolate (combine) multiple strings.
 - In JavaScript ES6, backticks (`) and ${} are used to interpolate values into a string.
