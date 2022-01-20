# Week 1 Day 2 Notes.

## Morning lecture notes

```
GitHub

- For your first commit, use git push u- origin master, this will allow you to use git push after when pushing to the main branch.

```

```js
// - Write a node program that takes in an unlimited number of command line arguments, goes through each and prints out the sum of them. If any argument is not a whole number, skip it. Do support negative numbers though. If any argument is not a number, output an error message. We need at least 2 arguments.

// Extract the command line arguments
// Edge Case:  We need at least 2 arguments.

const args = process.argv.slice(2);
// console.log("Args:", args);

if (args.length < 2) {
  console.log("Please enter at least 2 command line arguments");
  process.exit();
}

// add a placeholder

// function declaration
// function sum () {

// }

// ['1','2', ...]
const convertToNums = function (numbers) {
  let outputNums = [];
  for (let num of numbers) {
    // convert num to Number, Typecast
    outputNums.push(Number(num));
  }

  return outputNums;
};

const allNums = function (numbers) {
  for (let num of numbers) {
    // Edge case: If any argument is not a number, output an error message.
    if (isNaN(num)) {
      console.log("Please, enter only numbers");
      process.exit();
    }
  }
  return numbers;
};

const filterInts = function (numbers) {
  const outputNums = [];

  for (let num of numbers) {
    // Edge case: If any argument is not a whole number, skip it.
    // Number.isInteger
    // modulo operator % if num % 1 === 0
    if (Number.isInteger(num)) {
      outputNums.push(num);
    }
  }

  return outputNums;
};

// single responsibility principle
// a function should have a single goal

// function expression
const sum = function (numbers) {
  let total = 0;

  // goes through each and
  for (let num of numbers) {
    total += num;
    console.log("num:", num, "total:", total);
  }
  return total;
};

// prints out the sum of them

const result = sum(filterInts(allNums(convertToNums(args))));

console.log("Final Total:", result);
```

## Functions

- it is better to have multiple smaller functions vs one big function that does everything

### Rules for defining functions

- Give your functions precise verb/action based names

- Use camelCasedNames (like this one)

- Properly indent the function code

- Functions should focus on a single task: returning a value or causing a side effect. Break your function into additional smaller functions if you find it doing two or more things

  - One single task could be to compute and return a value (eg: zeroPad)

  - Another single task could be to perform a side effect such as logging a message to the screen (eg: printFarmInventory)

- Data needed by Functions should be passed in as parameters/arguments (i.e. local scope) instead of being accessed directly

## Scope

### Global vs Local Scope

Let's classify two basic levels of scope: global and local.

- A globally-scoped variable is available everywhere in the code,
- locally-scoped variable would only be available within the function in which it's defined.

### Scope can Overwrite Variables

```js
let myVar = "global";

const myFunction = function () {
  let myVar = "local";

  console.log("inside myFunction, myVar is:", myVar);
};

myFunction();

console.log("outside myFunction, myVar is:", myVar);
```

The local variable myVar takes precedence inside myFunction. It would evaluate to "local"
However outside the function the variable myVar behaves as a global variable. It would evaluate to "global"

## Coercion and Truthy/Falsey

### Double Equals, Triple Equals, and Type Coercion

The `===` does not only compare two values, but also the type of those values. Consider this example:

```js
23 === "23";
```

Even though both of the above values are 23, one is a String and the other is a Number. Before comparing the actual values, `===` will compare the types, see that they are not the same, and immediately return False without going any further.

```js
23 == "23";
```

In this case, `==` returns True. Before performing any sort of comparison, the `==` operator will attempt to force the two values to be of the same type, if possible. This is called `type coercion`,

## Truthy and Falsey

```js
// All of the following are inherently falsey:

False;
// False is False. Makes sense, right?

0;
// 0 is the only falsey Number

("");
// an empty string is falsey

null;
// a null, or empty value, is falsey.

undefined;
// an object that has not been defined is considered falsey.

NaN;
// Not a Number. You'll learn more about NaN as we go on.
```

This means that if it is evaluated, it will return `false`.
