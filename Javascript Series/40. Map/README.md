<h1 align='center'>~ Map ~</h1>

<p>A Map object is a simple key/value map and can iterate its elements in insertion order. You can create a new map like below.</p>

```javascript
var person = new Map();
```

<h3>Set Map Value</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
console.log(person);
// output Map { 'name' => 'Adam', 'age' => 14 }
```

<h3>Get Map Value</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
console.log(person.get('age'));
// output 14
```

<h3>Size of Map</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
console.log(person.size);
// output 2
```

<h3>Check if Item Exist in Map</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
console.log(person.has('age'));
console.log(person.has('phoneNumber'));
// output true, false
```

<h3>Delete Item in Map</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
person.delete('name');
console.log(person);
// output Map { 'age' => 14 }
```

<h3>Loop Map</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
for (let [key, value] of person) {
  console.log(key + ': ' + value);
}
// output name: Adam, age: 14
```

<h3>Clear Map</h3>

```javascript
var person = new Map();
person.set('name', 'Adam');
person.set('age', 14);
console.log(person);
// output Map { 'name' => 'Adam', 'age' => 14 }
person.clear();
console.log(person);
// output Map {  }
```

<h3>Object vs Map</h3>

<p>Traditionally, objects have been used to map strings to values. Objects allow you to set keys to values, retrieve those values, delete keys, and detect whether something is stored at a key. Map objects, however, have a few more advantages that make them better maps.</p>

<ul>
  <li>The keys of an Object are Strings or Symbols, where they can be of any value for a Map</li>
  <li>You can get the size of a Map easily, while you have to manually keep track of size for an Object</li>
  <li>The iteration of maps is in insertion order of the elements</li>
  <li>An Object has a prototype, so there are default keys in the map.</li>
</ul>

<h3>When to use Map</h3>

<ul>
  <li>Use maps over objects when keys are unknown until run time, and when all keys are the same type and all values are the same type.</li>
  <li>Use maps if there is a need to store primitive values as keys because object treats each key as a string whether it's a number value, boolean value or any other primitive value.</li>
  <li>Use objects when there is logic that operates on individual elements.</li>
</ul>
