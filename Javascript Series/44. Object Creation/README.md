<h1 align='center'>~ Object Creation ~</h1>

<p>There are three way to create objects in javascript.</p>

<ul>
  <li>Object Literal</li>
  <li>Constructor Function</li>
  <li>Object.create Method</li>
</ul>

<h3>Object Literal</h3>

```javascript
var person = {name : 'Adam', age : 18, phoneNumber : '234-344-2342'};
```

<h3>Constructor Function</h3>

<p>A constructor function is used to instantiate an object. By invoking that function with the new operator we can create new objects with it. To create new objects with the constructor function you can follow the below steps.</p>

<ul>
  <li>Define the object type by writing a constructor function.</li>
  <li>Create an instance of the object with new.</li>
</ul>

```javascript
function Person(name, age, phoneNumber) {
  this.name = name;
  this.age = age;
  this.phoneNumber = phoneNumber;
}
var person1 = new Person('Adam', 23, '434-344-6653');
var person2 = new Person('Steve', 13, '237-354-7654');
console.log(person1);
console.log(person2);
// output Person { name: "Adam", age: 23, phoneNumber: "434-344-6653" } 
// output Person { name: "Steve", age: 13, phoneNumber: "237-354-7654" } 
```

<p>You can create any number of objects using the constructor function you created. All the objects are independent on their own. Changes to one object does not affect any of the other objects. To add the new property to all objects of the same type, you have to add the property to the definition of the Person object type.</p>

<h3>Object.create Method</h3>

<p>Objects can also be created using the Object.create() method. This method can be very useful, because it allows you to choose the prototype object for the object you want to create, without having to define a constructor function. Prototype is simply inheritance. The object that is to be created has inherited the information from the object we passed in which is 'person' below.</p>

```javascript
var person = {name : 'Adam', age : 23, phoneNumber : '434-344-6653'};
var newPerson = Object.create(person);
newPerson.name = 'Steve';
console.log(newPerson.name);
console.log(newPerson.age);
console.log(newPerson.phoneNumber);
// output 'Steve', 23, '434-344-6653'
```
