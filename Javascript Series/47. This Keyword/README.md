<h1 align='center'>~ This Keyword ~</h1>

<p>JavaScript has a special keyword, this, that you can use within a method to refer to the current object.</p>

```javascript
var person = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
person.getName = function() {
  return this.name;
};
console.log(person.getName());
// output 'Adam'
```

<p>There are also three different types of bindings in javascript. Binding basically mean how this is reference depending on the context it was called in.</p>

<ul>
  <li>Explicit Binding</li>
  <li>Implicit Binding</li>
  <li>Default Binding</li>
</ul>

<h3>Explicit Binding</h3>

<p>Explicit binding of this occurs when .call(), .apply(), or .bind() are used on a function. We call these explicit because you are explicitly passing in a this context to call() or apply(). We’ll talk bind() in just a moment.</p>

<h4 align='center'>Call Method</h4>

<p>For call method we pass in the this we'd like to use, along with parameters.</p>

```javascript
var person1 = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
var person2 = {name : 'Jack', age : 21, phoneNumber : '453-769-4564'};

function getPersonFavoriteFood(fruit) {
  console.log(this.name + ' likes ' + fruit + '.');
}

getPersonFavoriteFood.call(person1, 'pizza'); // output 'Adam likes pizza.'
getPersonFavoriteFood.call(person2, 'candy'); // output 'Jack likes candy.'
```

<h4 align='center'>Apply Method</h4>

<p>The apply method is almost the same, except we must pass in an array of parameters after our this context.</p>

```javascript
var person1 = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
var person2 = {name : 'Jack', age : 21, phoneNumber : '453-769-4564'};

function getPersonFavoriteFood(fruit) {
  console.log(this.name + ' likes ' + fruit + '.');
}

getPersonFavoriteFood.apply(person1, ['pizza']); // output 'Adam likes pizza.'
getPersonFavoriteFood.apply(person2, ['candy']); // output 'Jack likes candy.'

```

<h4 align='center'>Bind Method</h4>

<p>When called on a function, .bind() sets a this context and returns a new function of the same name with a bound this context. Bind creates a persistent this context.</p>

```javascript
var person1 = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
var person2 = {name : 'Jack', age : 21, phoneNumber : '453-769-4564'};

function getPersonFavoriteFood(fruit) {
  console.log(this.name + ' likes ' + fruit + '.');
}

getPersonFavoriteFood.bind(person1)('pizza'); // output 'Adam likes pizza.'
getPersonFavoriteFood.bind(person2)('candy'); // output 'Jack likes candy.'
```

<h3>Implicit Binding</h3>

<p>Implicit binding occurs when dot notation is used to invoke a function. In implicit binding, whatever is to the left of the dot becomes the context for this in the function.</p>

```javascript
var person = {name : 'Adam', age : 34, phoneNumber : '345-242-4657'};
person.getName = function() {
  return this.name;
};
console.log(person.getName());
// output 'Adam'
```

<h3>Default Binding</h3>

<p>Default binding refers to how this is the global context whenever a function is invoked without any of the rules above. If we aren't using a dot and we aren't using call(), apply(), or bind(), our this will be our global object. Your global context depends on where you're working. If you're in the browser, this will be the window. When programming in strict mode, the global context is undefined.</p>

```javascript
function test() {
  console.log(this);
}
test();
// output [object Window] 
```
