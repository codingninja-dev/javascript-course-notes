<h1 align='center'>~ Logical Operators ~</h1>

<p>Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value.</p>

<table align="center">
  <thead>
    <tr align="center">
      <td><b>Operator</b></td>
      <td><b>Description</b></td>
      <td><b>Example</b></td>
    </tr>
  </thead>
  <tbody>
    <tr align="center">
      <td>Logical AND (&&)</td>
      <td>expr1 && expr2</td>
      <td>Returns expr1 if it can be converted to false; otherwise, returns expr2. Thus, when used with Boolean values, && returns true if both operands are true; otherwise, returns false.</td>
    </tr>
    <tr align="center">
      <td>Logical OR (||)</td>
      <td>expr1 || expr2</td>
      <td>Returns expr1 if it can be converted to true; otherwise, returns expr2. Thus, when used with Boolean values, || returns true if either operand is true; if both are false, returns false.</td>
    </tr>
    <tr align="center">
      <td>Logical NOT (!)</td>
      <td>!expr</td>
      <td>Returns false if its single operand that can be converted to true; otherwise, returns true.</td>
    </tr>
  </tbody>
</table>

<p>Examples of expressions that can be converted to false are those that evaluate to null, 0, NaN, the empty string (""), or undefined.</p>

<h3>And Operator</h3>

```javascript
var a1 =  true && true;     // t && t returns true
var a2 =  true && false;    // t && f returns false
var a3 = false && true;     // f && t returns false
var a4 = false && (3 == 4); // f && f returns false
var a5 = 'Cat' && 'Dog';    // t && t returns Dog
var a6 = false && 'Cat';    // f && t returns false
var a7 = 'Cat' && false;    // t && f returns false
```

<h3>Or Operator</h3>

```javascript
var o1 =  true || true;     // t || t returns true
var o2 = false || true;     // f || t returns true
var o3 =  true || false;    // t || f returns true
var o4 = false || (3 == 4); // f || f returns false
var o5 = 'Cat' || 'Dog';    // t || t returns Cat
var o6 = false || 'Cat';    // f || t returns Cat
var o7 = 'Cat' || false;    // t || f returns Cat

```

<h3>Not Operator</h3>

```javascript
var n1 = !true;  // !t returns false
var n2 = !false; // !f returns true
var n3 = !'Cat'; // !t returns false

```
