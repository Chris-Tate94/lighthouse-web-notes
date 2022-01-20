# Quick notes

## String Conversion

- Turning a string into a [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#Convert_numeric_strings_to_numbers)

## Compare two Arrays

- You cannot compare two arrays in Javascript
  ```javascript
  [1, 2, 3] === [1, 2, 3]; // => false
  ```

* A workaround is to use the [Array.every( )](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
  method. The `every()` method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

# Cheat code for checking if arrays are equal

```js
const eqArrays = function (arr1, arr2) {
  if (arr1 === arr2) {
    return true;
  }
  //edge case
  if (arr1 == null || arr2 == null) {
    return false;
  }
  //check if the arrays are the same length
  if (arr1.length !== arr2.length) {
    return false;
  }
  // loop through the first array and check that value against the same value in the second array
  for (let i = 0; i < arr1.length; i++) {
    if (arr1[i] !== arr2[i]) {
      return false;
    }
  }
  return true;
};
```

# HTTP Intro

- HTTP is a request-response protocol, where the client makes requests and the server sends responses

- HTTP is a text based protocol, making it easy to read and understand for humans

- HTTP requests must contain the verb/method (eg: GET) and the Path (eg: /about)

- HTTP requests aren't always to receive data, but sometimes to save data, like when we submit a form on a website. This is done via a POST instead of a GET

- Requests and responses both contain key-value based headers (eg: Accept-Language: fr, Content-Type: text/html, etc.)
