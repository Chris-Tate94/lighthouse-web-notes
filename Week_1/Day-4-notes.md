# Day 4 Notes

## Lecture Notes

- Functions with no `return` will always come back as `undefined`

## Array prototype - Map

```js
const lighthouses = [
  "Gibraltar Point",
  "Peggy's Point",
  "Cove Island",
  "Discovery Island",
  "Cape Scott",
  "Point Clark",
  "Kincardine",
];

const map1 = lighthouses.map((string) => string.length);

console.log(map1);

//will return [15, 13, 11, 16, 10, 11, 10];
```
