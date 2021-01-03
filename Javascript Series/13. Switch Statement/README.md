<h1 align='center'>~ Switch Statement ~</h1>

<p>A switch statement allows a program to evaluate an expression and attempt to match the expression's value to a case label. If a match is found, the program executes the associated statement.</p>

```javascript
var name = 'jack';

switch (name) {
  case 'jack':
    console.log('welcome jack');
    break;
  case 'jill':
    console.log('welcome jill');
    break;
  default:
    console.log('Name cannot be found');
}
```

<p>Remember, the optional break statement associated with each case clause ensures that the program breaks out of the switch once the matched statement is executed, and then continues execution at the statement following switch. If break is omitted, the program continues execution inside the switch statement (and will evaluate the next case, and so on).</p>

