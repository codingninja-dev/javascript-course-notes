<h1 align='center'>~ Unary Operators ~</h1>

<p>A unary operation is an operation with only one operand.</p>

<ul>
  <li>delete</li>
  <li>typeof</li>
</ul>

<h3>Delete Operator</h3>

<p>The delete operator deletes an object's property.</p>

```javascript
var person = {name : 'Adam', age : 25};
delete person.age;
console.log(person);
// output {name : 'Adam'}
```

<p>If the delete operator succeeds, it removes the property from the object. Trying to access it afterwards will yield undefined. The delete operator returns true if the operation is possible; it returns false if the operation is not possible.</p>

<h3>Typeof Operator</h3>

<p>The typeof operator returns a string indicating the type of the unevaluated operand. operand is the string, variable, keyword, or object for which the type is to be returned.</p>

```javascript
var messageFunc = function() { console.log('Hello World') };
var name = 'Adam';
var number = 1;
var list = [1, 2, 3];
var today = new Date();

typeof messageFunc; // output "function"
typeof name;        // output "string"
typeof number;      // output "number"
typeof list;        // output "object"
typeof today;       // output "object"
typeof doesntExist; // output "undefined"

```
