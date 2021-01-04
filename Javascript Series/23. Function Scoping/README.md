<h1 align='center'>~ Function Scoping ~</h1>

<p>Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.</p>

```javascript
var name = 'Adam';
function updateName(){
  var newName = 'Eve';
  console.log(name);
  console.log(newName);
}
updateName();
console.log(name);
console.log(newName);
// output 'Adam', 'Eve', 'Adam', and undefined
```

```javascript
var name = 'Adam';
function updateName(){
  var newName = 'Eve';
  console.log(name);
  console.log(newName);
  console.log(generatedName);
  function generateName() {
    var generatedName = 'Jim';
    console.log(generatedName);
  }
  generateName();
}
updateName();
console.log(name);
console.log(newName);
// output 'Adam', 'Eve', undefined, 'Jim', 'Adam', and undefined
```

<p>A function defined in the global scope can access all variables defined in the global scope. A function defined inside another function can also access all variables defined in its parent function, and any other variables to which the parent function has access. This will not work if you are trying to access your inner child's function variables from your outer parent function. If you see in the above code the variable 'generatedName' is not available outside of the 'updateName' function but its available inside the 'generateName' function.</p>
