<h1 align='center'>~ Object Setter & Getter ~</h1>

<p>In JavaScript, there are two kinds of object properties:</p>

<ul>
  <li>Data properties</li>
  <li>Accessor properties</li>
</ul>

<p>Data properties are properties in an object like below.</p>

```javascript
var person = {
  // data property
  name : 'Adam'
};
```

<p>Accessor properties are methods that get or set the value of an object. For that, we use these two keywords:</p>

<ul>
  <li>get - to define a getter method to get the property value</li>
  <li>set - to define a setter method to set the property value</li>
</ul>

<p>A getter is a method that gets the value of a specific property. A setter is a method that sets the value of a specific property. You can define getters and setters on any predefined core object or user-defined object that supports the addition of new properties.</p>

<h3>Getter Example</h3>

<p></p>

```javascript
var person = {
  name : 'Adam',
  age : 34,
  phoneNumber : '345-242-4657',
  get getName() {
    return this.name;
  }
};

console.log(person.getName);
// output 'Adam'
```

<h3>Setter Example</h3>

<p></p>

```javascript
var person = {
  name : 'Adam',
  age : 34,
  phoneNumber : '345-242-4657',
  get getName() {
    return this.name;
  },
  set setName(name) {
    this.name = name;
  }
};
person.setName = 'Calvin';
console.log(person.getName);
// output 'Calvin'
```
