<h1 align='center'>~ Closure ~</h1>

<p>You may nest a function within another function. The nested (inner) function is private to its containing (outer) function. This will also form a closure. What this means is that any arguments or variables that are declared in the outer function is accessible(or preserved) for the inner function.</p>

<ul>
  <li>The inner function can be accessed only from statements in the outer function</li>
  <li>The inner function form a closure. The inner function can use the arguments and variables of the outer function, while the outer function cannot use the arguments and variables of the inner function</li>
</ul>

```javascript
var counter = function () {
  var counter = 0;
  function updateCounter() {
    counter++; 
    return counter;
  }
  return updateCounter;
};

var counter1 = counter();
console.log(counter1());
console.log(counter1());
// output 1, 2

var counter2 = counter();
console.log(counter2());
console.log(counter2());
console.log(counter2());
// output 1, 2, 3
```
<p>In the above example we are creating two separate counters 'counter1' and 'counter2' to keep track of two separate counters. Each counter preserve the state of the outer function separately in the two counter variables. Based on this we can guarantee the below.</p>
<ul>
  <li>A closure must preserve the arguments and variables in all scopes it references (updateCounter function is a closure)</li>
  <li>Since each call provides potentially different arguments, a new closure is created for each call to outside (counter1 and counter2)</li>
  <li>The memory used by the computer to store the closure for the updateCounter function can be freed only when the updateCounter function being returned from the counter function is no longer accessible</li>
</ul>

<h3>Naming Conflict</h3>

<p>When two arguments or variables in the scopes of a closure have the same name, there is a name conflict. More nested scopes take precedence. So, the inner-most scope takes the highest precedence, while the outer-most scope takes the lowest. This is the scope chain. The first on the chain is the inner-most scope, and the last is the outer-most scope.</p>

```javascript
function outside() {
  var x = 10;
  function inside(x) {
    return x * 2;
  }
  return inside;
}
var inside = outside();
var answer = inside(5);
console.log(answer);
// returns 10 instead of 20
```

<p>It first checks if inside function has the x if not it will check if outside function has the x and if x is not there it will check the global scope.</p>
