# Lecture Notes

## Set Time out

```js
console.log("first line");
setTimeout(() => {
  console.log("timeout line");
}, 5000);
console.log("last line");
```

- This will print out the below, with `timeout line` being printed with a 5000 milisecond delay (5 seconds). The timeout line will only execute after the delay (5000), meaning that the `first line` and `last line` will run instantly, then after 5 seconds, the timeout line will run.

```
first line
last line
timeout line
```
