<h1 align='center'>~ Variable Scoping ~</h1>

<p>When your working with variables there is something called variable scoping. It basically means the visibility of this variable to different parts of your code. The below are the three types of scoping we will focus on.</p>

<ul>
  <li>Global scope (your entire application)</li>
  <li>Block scope (loops and conditional statements)</li>
  <li>Function scope (functions)</li>
</ul>

<h3>Global Scope</h3>
<p>Any variable you declare in a script that is not in a function or a block statement is consider global scope. If you leave out the var, let, or const on a variable javascript will scope it to the global scope. This will apply to both block and function statements when keywords are left out.</p>

```javascript
if (true){
  name = 'Eve';
}
console.log(name); // Eve
```

```javascript
function setName (){
  name = 'Eve';
}
setName();
console.log(name); // Eve
```

<h3>Block Scope</h3>
<p>Below is an example of block scope and the name variable in the global scope being changed.</p>

```javascript
var name = 'Adam';
if (true){
  var name = 'Eve';
}
console.log(name); // Eve
```

<p>To fix this problem you can use let instead so it is scoped correctly. Both let and cost keyword will treat block scope as if they were function scoped.</p>


```javascript
var name = 'Adam';
if (true){
  let name = 'Eve';
}
console.log(name); // Adam
```

<h3>Function Scope</h3>
<p>Below is an example of function scope and the name variable in the global scope is not changed at all.</p>

```javascript
var name = 'Adam';
function setName (){
  var name = 'Eve';
}
setName();
console.log(name); // Adam
```
