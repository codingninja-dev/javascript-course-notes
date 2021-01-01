<h1 align='center'>~ Hoisting ~</h1>

<p>In javascript variable declaration and function declaration are hoisted to the top of the application. If you are in a function they are hoisted (to bring up) to the top of the function instead. See below on the different hoisting examples.</p>

<h3>Variable Hoisting</h3>

```javascript
console.log(name); // undefined
var name = 'Adam';
```

<p>Javascript will move any variable or function declaration to the top behind the scenes when your script runs.</p>

```javascript
var name;
console.log(name); // undefined
var name = 'Adam';
console.log(name); // Adam
```

<h3>Function Hoisting</h3>

```javascript
getName();
function getName() {
  console.log('Adam');
}
console.log('Eve');
```

<p>The above will output Adam and then followed by Eve. The below is whats happening behind the scenes.</p>

```javascript
function getName() {
  console.log('Adam');
}
getName();
console.log('Eve');
```

<h3>Variable Hoisting in Functions</h3>

```javascript
function getName() {
  var name;
  console.log(name); // undefined
  var name = 'Adam';
  console.log(name); // Adam
}
getName();
```

<p>Remember that depending on the scoping of the variable of where you declared the variable it will be hoisted differently in block scope and function scope.</p>
