<h1 align='center'>~ Function Expression ~</h1>

<p>Function expressions are same as function declaration except that they are stored in a variable.</p>

```javascript
var getName = function() {
  console.log('Adam');
};
getName();
// output 'Adam'
```

<p>The function you store in a variable can have a name or be anonymous.</p>

<h3>Anonymous Function Expression</h3>

```javascript
var getName = function() {
  console.log('Adam');
};
getName();
// output 'Adam'
```

<h3>Named Function Expression</h3>

```javascript
var getName = function retrieveName() {
  console.log('Adam');
};
getName();
// output 'Adam'
```

<p>Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces when your trying to find an issue in your code.</p>
<p>Function expressions are convenient when passing a function as an argument to another function. </p>

```javascript
function load(f) {
  f();
}
var getName = function retrieveName() {
  console.log('Adam');
};
load(getName);
// output 'Adam'
```
