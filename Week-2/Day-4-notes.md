# Day 4 Notes

# `JSON`

- stands for JavaScript Object Notation
- An Object encoded using JSON looks like this:

```js
{
  "name": "New York City",
  "boroughs": [
    "Manhattan",
    "Queens",
    "Brooklyn",
    "The Bronx",
    "Staten Island"],
  "population": 8491079,
  "area_codes": [212, 347, 646, 718, 917, 929],
  "position": { "lat": 40.7127, "lng": -74.0059 }
}
```

`The JSON syntax is (and must be) valid JavaScript.`

Note that the keys are always double-quoted "strings", and the values can be numbers, strings, or objects themselves.

The process of [serialization](https://en.wikipedia.org/wiki/Serialization) converts objects (or data structures) into a format that can be stored or transmitted between computers (typically as a string of text). The opposite, going from `String → Object` is called deserialization.

In JavaScript, we have the JSON object for serializing and deserializing. The Mozilla Developer Network (MDN) provides good [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON#Methods) on these two important methods:

# `JSON.parse()`

Parse a string as JSON, optionally transform the produced value and its properties, and return the value.

# `JSON.stringify()`

Return a JSON string corresponding to the specified value, optionally including only certain properties or replacing property values in a user-defined manner.
