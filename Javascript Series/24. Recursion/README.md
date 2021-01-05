<h1 align='center'>~ Recursion ~</h1>

<p>Recursion is a function that can refer to and call itself. There are two ways for a function to refer to itself:</p>

<ul>
  <li>The function's name</li>
  <li>An in-scope variable that refers to the function</li>
</ul>

<h3>The function's name</h3>

```javascript
function factorial(number) {
  if(number === 1) {
    return 1;
  } else {
    return number * factorial(number - 1);
  }
}
console.log(factorial(5));
// outputs 120
```

<h3>An in-scope variable that refers to the function</h3>

```javascript
var factorial = function(number) {
  if(number === 1) {
    return 1;
  } else {
    return number * factorial(number - 1);
  }
};
console.log(factorial(5));
// outputs 120
```

<p>A function that calls itself is called a recursive function. In some ways, recursion is very similar to loops. Both execute the same code multiple times, and both require a condition (to avoid an infinite loop, or rather, infinite recursion in this case).</p>
