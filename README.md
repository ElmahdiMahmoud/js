JavaScript - Exercises, Solution
==

## JavaScript functions

##### function that reverse a number.
```js
/* [ JavaScript function that reverse a number. ] */
function reverse_a_number(x){
	x = x + "";
	return x.split("").reverse().join("");
}
console.log(reverse_a_number(12345)); // 54321
```

##### function that generates all combinations of a string.
```js
/* [ JavaScript function that generates all combinations of a string. ] */
function substrings(str){
  var substr = [];
  for (var x = 0; x < str.length; x++) {
    for (var y = x + 1; y <= str.length; y++) {
      substr.push(str.substring(x,y));
    }
  }
 return substr;
}
console.log(substrings("red")); // ["r", "re", "red", "e", "ed", "d"]
```
