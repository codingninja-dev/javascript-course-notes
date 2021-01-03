<h1 align='center'>~ While Loop ~</h1>

<p>A while statement executes its statements as long as a specified condition evaluates to true.</p>

```javascript
var x = 1;

while(x <= 10) {
  console.log(x);
  x++;
} 
```
<p>If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.</p>

<p>The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.</p>

<h3>Infinite Loops</h3>

```javascript
var condition = true;

while(condition) {
  console.log('hello world');
} 
```
<p>'hello world' is outputed everytime the loops runs in the above code. The above code is called an infinite loop becuase the loop never ends. Make sure to always create loops that ends.</p>

