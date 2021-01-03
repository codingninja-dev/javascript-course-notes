<h1 align='center'>~ Do While Loop ~</h1>

<p>The do...while statement repeats until a specified condition evaluates to false. However, the statement in the 'do' is always executed once before the condition is checked.</p>

```javascript
var x = 0;
do
  x++;
  console.log(x);
while (x <= 10);
// will output number from 1 - 10
```
<h3>Do Action Only</h3>

```javascript
do
  console.log('hello world');
while (false);
// hello world is outputed and loop is checked and since its false it will end
```
