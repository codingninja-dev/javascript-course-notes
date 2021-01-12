<h1 align='center'>~ Object Prototype ~</h1>

<p>Object prototype is object inheritance in javascript. It allows an object to create inheritance with other objects. The analogy we can use to describe prototype inheritance in javascript is child parent relationship.The child object has access to its parent object. Any variable or function on a parent object is accessible to the child object.</p>

<p>We can create objects in the constructor function or the prototype of the Person constructor. The drawback of adding the method to the constructor function instead of the prototype is that the method in the constructor is created everytime an object is created while the prototype only creates it one time and all object created will continue to access the method from the prototype of the object.</p>

```javascript
function Person(name, age, phoneNumber) {
  this.name = name;
  this.age = age;
  this.phoneNumber = phoneNumber;
}

Person.prototype.getName = function() {
  return this.name;
};

var person = new Person('Adam', 23, '434-344-6653');
console.log(person.getName());
// output 'Adam'
```

<p>We are creating a new object with a constructor function and then we are using the object.create method to create a brand new object that has the Person object we created as it's prototype. The new object inherits from the person object.</p>

```javascript
function Person(name, age, phoneNumber) {
  this.name = name;
  this.age = age;
  this.phoneNumber = phoneNumber;
}

Person.prototype.getName = function() {
  return this.name;
};

var person = new Person('Adam', 23, '434-344-6653');
var newPerson = Object.create(person);
console.log(newPerson.name);
console.log(newPerson.age);
console.log(newPerson.phoneNumber);
console.log(newPerson.getName());
// output 'Adam', 23, '434-344-6653', 'Adam'
```
