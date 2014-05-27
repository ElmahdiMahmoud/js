JavaScript - Exercises, Solution
==

## JavaScript functions

##### JavaScript function that reverse a number.
```js
/* [ JavaScript function that reverse a number. ] */
function reverse_a_number(x){
	x = x + "";
	return x.split("").reverse().join("");
}
console.log(reverse_a_number(12345)); // 54321
```
