# Recursion

```js
1.| function countEvenToTwelve(number) {
2.|   if (number <= 12) {
3.|     console.log(number);
4.|     countEvenToTwelve(number+2);
5.|   }
6.| }
7.| countEvenToTwelve(0);
```

As long as `number <= 12`, the function continues to call itself to repeat the code over and over again. As soon as `number > 12`, the function stops calling itself and the "looping" ends.

Each time `countEvenToTwelve` calls itself, on line 4, it passes in a different input value. In this case, each time the function is called, `number` will be 2 more than it was the last time. So the first time the function is called, number is equal to `0`. The second time it's called, number is equal to `2`, and so on. Instead of incrementing the number directly, like in the loop, the function calls itself again with a modified input parameter. Every time the function calls itself, `number` gets bigger and bigger. This is important, because the function will only stop calling itself when number is greater than 12.

Every recursive function `must stop calling itself at some point`, otherwise it will just continue to call itself forever, like an infinite loop. The following function never stops calling itself.

## Infinite Recursive function

```js
function countUpFrom(number) {
  console.log(number);
  countUpFrom(number + 1);
}
countUpFrom(1);
```

We refer to `number <= 12 as a recursive case`, because as long as this is true, the function will continue to call itself.

We refer to n`umber > 12 as a base case.` If this is true, the function will not call itself.
The recursive case is when the function will continue to call itself. Every time the function calls itself, the input gets closer and closer to the base case. The base case is when the function no longer calls itself. In a properly designed recursive function, with each recursive call, the input must gradually resolve toward the base case.

A function must have at least one recursive case and at least one base case in order to be recursive.

```js 1.| function countEvenToTwelve(number) {
2.|   if (number <= 12) { // Recursive Case
3.|     console.log(number);
4.|     // The function will call itself again and get closer to the base case
5.|     countEvenToTwelve(number+2);
6.|   }
7.|   // Base case, do nothing when number > 12
8.| }
9.| countEvenToTwelve(0);
```
