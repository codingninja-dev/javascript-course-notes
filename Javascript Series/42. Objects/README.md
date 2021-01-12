<h1 align='center'>~ Objects ~</h1>

<p>An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method. In addition to objects that are predefined in the browser, you can define your own objects.</p>

<p>Objects in JavaScript, just as in many other programming languages, can be compared to objects in real life. The concept of objects in JavaScript can be understood with real life, tangible objects. In JavaScript, an object is a standalone entity, with properties and type. Compare it with a car, for example. A car is an object, with properties. A car has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.</p>

<h3>Create Empty Object</h3>

```javascript
var person = {};
```

<h3>Create non-empty Object</h3>

```javascript
var person = {name : 'Adam', age : 23, phoneNumber : '234-234-2342'};
```

<h3>Assigning Property (Dot Notation)</h3>

```javascript
var person = {};
person.name = 'Adam';
console.log(person);
// output  {name: "Adam"} 
```

<h3>Assigning Property (Bracket Notation)</h3>

```javascript
var person = {};
person['name'] = 'Adam';
console.log(person);
// output  {name: "Adam"} 
```

<p>An object property name can be any valid JavaScript string, or anything that can be converted to a string, including the empty string. However, any property name that is not a valid JavaScript identifier (for example, a property name that has a space or a hyphen, or that starts with a number) can only be accessed using the square bracket notation. This notation is also very useful when property names are to be dynamically determined (when the property name is not determined until runtime).</p>

<h3>Add Method to Object</h3>

```javascript
var person = {name : 'Adam', age : 18};
person.getAge = function() {
  return this.age;
};
console.log(person.getAge());
// output  18
```
