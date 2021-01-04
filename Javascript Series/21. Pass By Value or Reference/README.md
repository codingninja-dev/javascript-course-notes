<h1 align='center'>~ Pass By Value or Reference ~</h1>

<h3>Pass By Value</h3>
<p>Primitive parameters (such as a number) are passed to functions by value; the value is passed to the function, but if the function changes the value of the parameter, this change is not reflected globally or in the calling function.</p>

```javascript
var name = 'Adam';

function changeName(name) {
  name = 'Eve';
}

changeName(name);
console.log(name);
// output 'Adam'
```

<h3>Pass By Reference</h3>
<p>If you pass an object (i.e. a non-primitive value, such as Array or a user-defined object) as a parameter and the function changes the object's properties, that change is visible outside the function</p>

```javascript
var person = {name : 'Adam', age : 16, phoneNumber : '234-453-3345'};

function updatePerson(person) {
  person.name = 'Eve';
}

updatePerson(person);
console.log(person); 
// output {name : 'Eve', age : 16, phoneNumber : '234-453-3345'}
```
