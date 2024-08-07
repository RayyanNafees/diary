
- Taken from [can u break a .forEach loop](https://javascript.plainenglish.io/javascript-interview-can-you-stop-or-break-a-foreach-loop-9608ba2a1710)
-
- `[].some()` - is like `.forEach()` but breaks if u return a `truthy` value
```js
// will run
[1,2,3,4].some((i,n)=>{
console.log(i,n)
})

// will break after first
[1,2,3,4].some(i => i+1)
```
- `[].every() `- is like `.forEach()` but breaks if u return a `falsy` value
```js
// will run
[1,2,3,4].every(i => i+1)

// will break after first
[1,2,3,4].every((i,n)=>{
console.log(i,n)
})
```
- Remember them as _"Some people are True, but Every one is False"_
- Use `return` in a regular `[].forEach()` loop and it acts like a `continue`
- `[].entries()` pattern
```js
let sparseArray = [1, , 3, , 5];

for (const [index, num] of sparseArray.entries()) {
  console.log(`Index ${index}: ${num}`);}

```