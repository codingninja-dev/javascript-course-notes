<h1 align='center'>~ Object Looping ~</h1>

<p>There are a few ways to traverse object properties.</p>

<ul>
  <li>for...in</li>
  <li>Object.keys(o)</li>
  <li>Object.values(o)</li>
  <li>Object.entries(o)</li>
  <li>Object.getOwnPropertyNames(o)</li>
</ul>

<h3>for...in Loop</h3>

<p>The for...in statement iterates over all enumerable properties of an object that are keyed by strings, including inherited enumerable properties.</p>

```javascript
var person = {name : 'Adam', age : 18};
for(var key in person) {
  console.log(person[key]);
}
// output 'Adam', 18
```

<h3>Object.keys(o)</h3>

<p>The Object.keys() method returns an array of a given object's own enumerable property names, iterated in the same order that a normal loop would.</p>

```javascript
var person = {name : 'Adam', age : 18};
console.log(Object.keys(person));
// output ["name", "age"] 
```

```javascript
var person = {name : 'Adam', age : 18};
for(var key of Object.keys(person)) {
  console.log(person[key]);
}
// output 'Adam', 18
```

<h3>Object.values(o)</h3>

<p>The Object.values() method returns an array of a given object's own enumerable property values, in the same order as that provided by a for...in loop. (The only difference is that a for...in loop enumerates properties in the prototype chain as well.)</p>

```javascript
var person = {name : 'Adam', age : 18};
console.log(Object.values(person));
// output ["Adam", 18] 
```

```javascript
var person = {name : 'Adam', age : 18};
for(var value of Object.values(person)) {
  console.log(value);
}
// output 'Adam', 18
```

<h3>Object.entries(o)</h3>

<p>The Object.entries() method returns an array of a given object's own enumerable string-keyed property [key, value] pairs, in the same order as that provided by a for...in loop.</p>

```javascript
var person = {name : 'Adam', age : 18};
console.log(Object.entries(person));
// output [ [ 'name', 'Adam' ], [ 'age', 18 ] ]
```

```javascript
var person = {name : 'Adam', age : 18};
for(var property of Object.entries(person)) {
  console.log('Key: ' + property[0] + ', Value: ' + property[1]);
}
// output 'Key: name, Value: Adam', 'Key: age, Value: 18'
```

<h3>Object.getOwnPropertyNames(o)</h3>

<p>The Object.getOwnPropertyNames() method returns an array of all properties (including non-enumerable properties except for those which use Symbol) found directly in a given object.</p>

```javascript
var person = {name : 'Adam', age : 18};
console.log(Object.getOwnPropertyNames(person));
// output ["name", "age"] 
```

```javascript
var person = {name : 'Adam', age : 18};
for(var key of Object.getOwnPropertyNames(person)) {
  console.log(person[key]);
}
// output 'Adam', 18
```
