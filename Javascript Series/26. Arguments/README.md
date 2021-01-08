<h1 align='center'>~ Arguments ~</h1>

<p>The arguments of a function are maintained in an array-like object.</p>

```javascript
function outputNames(name1, name2, name3) {
  console.log(arguments);
}

outputNames('Adam', 'Jack', 'Jill');
// output {0: "Adam" , 1: "Jack" , 2: "Jill"} 
```

<p>To get the length of the argument list you can use the property below to access the length.</p>

```javascript
function outputNames(name1, name2, name3) {
  console.log(arguments.length);
}

outputNames('Adam', 'Jack', 'Jill');
// output 3
```

<p>Using the arguments object, you can call a function with more arguments than it is formally declared to accept. This is often useful if you don't know in advance how many arguments will be passed to the function. You can use arguments.length to determine the number of arguments actually passed to the function, and then access each argument using the arguments object.</p>

```javascript
function add() {
  var sum = 0;
  for (var x = 0 ; x < arguments.length ; x++) {
    sum = sum + arguments[x];
  }
  console.log(sum);
}

add(1,2,3,4,5);
// output 15
```


```javascript
function add() {
  var sum = 0;
  for(var number of arguments) {
    sum = sum + number;
  }
  console.log(sum);
}
add(1,2,3,4,5);
// output 15
```

<p>You want to keep in mind that the arguments variable is "array-like", but not an array. It is array-like in that it has a numbered index and a length property. However, it does not possess all of the array-manipulation methods(similar to functions).</p>
