<h1 align='center'>~ Relational Operators ~</h1>

<p>A relational operator compares its operands and returns a Boolean value based on whether the comparison is true.</p>

<ul>
  <li>in</li>
  <li>instanceof</li>
</ul>

<h3>In Operator</h3>

<p>The in operator returns true if the specified property is in the specified object.</p>

```javascript
var list = ['orange', 'apple', 'pear'];
var person = {name : 'Adam', age : 23};
console.log('orange' in list);  // false
console.log(0 in list);         // true
console.log('name' in person);  // true
console.log(45 in list);        // false
```

<h3>Instanceof Operator</h3>

<p>The instanceof operator returns true if the specified object is of the specified object type. Use instanceof when you need to confirm the type of an object at runtime.</p>

<p>For example, the following code uses instanceof to determine whether theDay is a Date object. Because theDay is a Date object, the console returns true.</p>

```javascript
var theDay = new Date();
console.log(theDay instanceof Date);
// output true
```
