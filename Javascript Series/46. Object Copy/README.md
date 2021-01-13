<h1 align='center'>~ Object Copy ~</h1>

<p>There are two different kind of copy in javascript. There is the shallow copy and there is the deep copy. If a property has a value as an array or object what shallow copy does is that it copies the reference. However, for deep copy it will actually create an entirely new array or object instead of copying it as a reference.</p>

<ul>
  <li>Shallow Copy</li>
  <li>Deep Copy</li>
</ul>

<h3>Copy by Equal (=)</h3>

<p>Because objects in JavaScript are reference values, you can't simply just copy using the =. You can see in the bottom that when you assign new values for the 'newPerson' object the values are updated in the main 'person' object. That's because Objects are reference types. So when you use =, it copied the pointer to the memory space it occupies. Reference types don't hold values, they are a pointer to the value in memory.</p>

```javascript
var person = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
var newPerson = person;
newPerson.name = 'Jack';
newPerson.age = 23;
newPerson.phoneNumber = '234-775-2234';
console.log(person);
console.log(newPerson);
// output { name: "Jack", age: 23, phoneNumber: "234-775-2234" } 
// output { name: "Jack", age: 23, phoneNumber: "234-775-2234" } 
```

<h3>Shallow Copy (Object.assign)</h3>

<p>The object.assign method is a great way to do a shallow copy of any object. For the first parameter of the Object.assign we used an empty object as the first argument, this will ensure you don't mutate (change) the original object.</p>

```javascript
var person = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
var newPerson = Object.assign({}, person);
newPerson.name = 'Jack';
newPerson.age = 23;
newPerson.phoneNumber = '234-775-2234';
console.log(person);
console.log(newPerson);
// output { name: "Adam", age: 34, phoneNumber: "345-242-4657" } 
// output { name: "Jack", age: 23, phoneNumber: "234-775-2234" } 
```

<h3>Deep Copy (JSON Parse/Stringify)</h3>

<p>This final way will give you a deep copy. Now I will mention, this is a quick and dirty way of deep cloning an object. For a more robust solution it is best to choose a library that provide support for object deep copy.</p>

```javascript
var person = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
var newPerson = JSON.parse(JSON.stringify(person));
newPerson.name = 'Jack';
newPerson.age = 23;
newPerson.phoneNumber = '234-775-2234';
console.log(person);
console.log(newPerson);
// output { name: "Adam", age: 34, phoneNumber: "345-242-4657" } 
// output { name: "Jack", age: 23, phoneNumber: "234-775-2234" } 
```

