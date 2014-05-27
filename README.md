JavaScript - Exercises, Solution
==

## JavaScript functions

```js
/* function that reverse a number. */
function reverse_a_number(x){
	x = x + "";
	return x.split("").reverse().join("");
}
console.log(reverse_a_number(12345)); // 54321
```

```js
/* function that generates all combinations of a string. */
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
/* function that returns a passed string with letters in alphabetical order. Assume punctuation 
   and numbers symbols are not included in the passed string. */

function alphabet_order(str){
 return str.split('').sort().join('');
} 
console.log(alphabet_order("webmaster"));  // abeemrstw
```

```js
/* function that accepts a string as a parameter and converts the first letter of each word 
   of the string in upper case. */

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

```js
/* function that accepts a string as a parameter and find the longest word within the string. */

function find_longest_word(str) {
  var array = str.match(/\w[a-z]{0,}/gi),
      result = array[0];

  for(var x = 1 ; x < array.length ; x++) {
    if(result.length < array[x].length) {
    	result = array[x];
    } 
  }
  return result;
}
console.log(find_longest_word('Web Development Tutorial')); // Development
```

```js
/* function that accepts one argument and returns the type. */
function detect_data_type(value) {
var dtypes = [Function, RegExp, Number, String, Boolean, Object], x, len;
    
if (typeof value === "object" || typeof value === "function") {
	for (x = 0, len = dtypes.length; x < len; x++) {
		if (value instanceof dtypes[x]){ 
			return dtypes[x]; 
		}
	}
}
	return typeof value;
}
console.log(detect_data_type(12)); // number
console.log(detect_data_type('w3resource')); // string
console.log(detect_data_type(false));  // boolean
```
