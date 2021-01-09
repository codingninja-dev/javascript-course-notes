<h1 align='center'>~ Conditional Operator ~</h1>

<p>The conditional operator or the ternary operator is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition.</p>

```javascript
condition ? val1 : val2
```

<p>If condition is true, the operator has the value of val1. Otherwise it has the value of val2. You can use the conditional operator anywhere you would use a standard operator.</p>

```javascript
var age = 16;
var status = (age >= 18) ? 'adult' : 'minor';
console.log(status);
// output minor
```

<p>This statement assigns the value "adult" to the variable status if age is eighteen or more. Otherwise, it assigns the value "minor" to status.</p>
