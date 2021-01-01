<h1 align='center'>~ Constant Variable ~</h1>

<p>Constant variables are read-only. So once you declare it the variable cannot be changed again. Constant variable must be declared when you initialize your variable.</p>

<p>There are two different type of data you can store in variable. Primitive and non primitive data types (data stored in a variable).</p>

<ul>
  <li>Primitive Data Types (String, Number, Boolean, Undefined, and Null)</li>
  <li>Non-Primitive Data Types (Objects and Arrays)</li>
</ul>

<h3>Primitive Data Types</h3>

```javascript
const name = 'Adam';
name = 'Eve';        // Will throw an error when script is run
```

```javascript
const name = 'Adam'; // No issue here
```

<h3>Non-Primitive Data Types</h3>

```javascript
const person = { 
  name : 'Adam',
  age : 23,
  phoneNumber : '(123)543-4543'
};                   // Object Data Type
person = 'Adam';     // Wrong (We are changing the constant variable directly)
person.name = 'Eve'; // Correct (We are changing the object instead of the variable itself)
```

```javascript
const numbers = [1,2,3]; // Array Data Type 
numbers = 1;             // Wrong (We are changing the constant variable directly)
numbers[0] = 5;          // Correct (We are changing the array instead of the variable itself)
```
