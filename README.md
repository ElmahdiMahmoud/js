JavaScript - Exercises, Solution
==

## JavaScript functions

```js
/* [ function that reverse a number. ] */
function reverse_a_number(x){
	x = x + "";
	return x.split("").reverse().join("");
}
console.log(reverse_a_number(12345)); // 54321
```

```js
/* [ function that generates all combinations of a string. ] */
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

```js
/* 
   function that returns a passed string with letters in alphabetical order. 
   Assume punctuation and numbers symbols are not included in the passed string. 
   */

function alphabet_order(str){
 return str.split('').sort().join('');
} 
console.log(alphabet_order("webmaster"));  // abeemrstw
```

```js
/* function that accepts a string as a parameter and converts the first letter 
   of each word of the string in upper case.
   */

function uppercase(str){
  var array = str.split(' '),
      newarray = [];

  for(var x = 0; x < array.length; x++){
      newarray.push(array[x].charAt(0).toUpperCase()+array[x].slice(1));
  }
  return newarray.join(' ');
}
console.log(uppercase("this is a lowercase")); // This Is A Lowercase
```
