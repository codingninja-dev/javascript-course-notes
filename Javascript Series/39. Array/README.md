<h1 align='center'>~ Array ~</h1>

<p>An array is an ordered list of values that you refer to with a name and an index. The bracket syntax is called an "array literal".</p>

```javascript
var list = [1, 2, 3];
console.log(list);
// output [1, 2, 3]
```

<p>1, 2, and 3 is a list of values for the array's elements. When these values are specified, the array is initialized with them as the array's elements. The array's length property is set to the number of arguments.</p>

```javascript
var list = [1, 2, 3];
console.log(list.length);
// output 3
```

<h3>Accessing Array Elements</h3>

<p>Elements in an array can be accessed by the index(numbered index). The index of the elements begins with zero.</p>

```javascript
var list = [1, 2, 3];
console.log(list[0]);
console.log(list[1]);
console.log(list[2]);
// output 1, 2, 3
```

<h3>Populating an Array</h3>

<p>You can populate an array by assigning values to its elements. For example:</p>

```javascript
var list = [1, 2, 3];
list[3] = 4;
list[4] = 5;
console.log(list);
// output [1, 2, 3, 4, 5]
```

<h3>Understanding length in Arrays</h3>

<p>At the implementation level, JavaScript's arrays actually store their elements as standard object properties, using the array index as the property name. The length property is special. It always returns the index of the last element plus one. Remember, JavaScript Array indexes are 0-based: they start at 0, not 1. This means that the length property will be one more than the highest index stored in the array:</p>

```javascript
var list = [];
list[3] = 4;
list[4] = 5;
console.log(list);
console.log(list.length);
// output [undefined, undefined, undefined, 4, 5], 5
```

<h3>Iterating Over Arrays</h3>

<p>A common operation is to iterate over the values of an array, processing each one in some way. The simplest way to do this is with loops.</p>

```javascript
var list = [1, 2, 3];
for (let x = 0; x < list.length; x++) {
  console.log(list[x]);
}
// output 1, 2, 3
```

```javascript
var list = [1, 2, 3];
list.forEach(function(item, idex) {
  console.log(item);
});
// output 1, 2, 3
```

```javascript
var list = [1, 2, 3];
for (let item of list) {
  console.log(item);
}
// output 1, 2, 3
```

<h3>Array Methods</h3>

<p>Here are some sample methods below. If you want the full list visit js documentation for more info.</p>

<h4>Concat</h4>
<p>Concat joins two or more arrays and returns a new array.</p>

```javascript
var list = [1, 2, 3];
console.log(list.concat([4, 5]));
// output '1, 2, 3, 4, 5'
```

<h4>Join</h4>
<p>Joins all elements of an array into a string.</p>

```javascript
var list = [1, 2, 3];
console.log(list.join(', '));
// output '1, 2, 3'
```

<h4>Push</h4>
<p>Push adds one or more elements to the end of an array and returns the resulting length of the array.</p>

```javascript
var list = [1, 2, 3];
list.push(4);
console.log(list);
// output '1, 2, 3, 4'
```

<h4>Pop</h4>
<p>Pop removes the last element from an array and returns that element.</p>

```javascript
var list = [1, 2, 3];
list.pop();
console.log(list);
// output '1, 2'
```

<h4>Shift</h4>
<p>Shift removes the first element from an array and returns that element.</p>

```javascript
var list = [1, 2, 3];
list.shift();
console.log(list);
// output '2, 3'
```

<h4>Unshift</h4>
<p>Unshift adds one or more elements to the front of an array and returns the new length of the array.</p>

```javascript
var list = [1, 2, 3];
list.unshift(0);
console.log(list);
// output '0, 1, 2, 3'
```

<h4>Reverse</h4>
<p>Reverse transposes the elements of an array, in place: the first array element becomes the last and the last becomes the first. It returns a reference to the array.</p>

```javascript
var list = [1, 2, 3];
list.reverse();
console.log(list);
// output '3, 2, 1'
```

<h4>Sort</h4>
<p>Sort sorts the elements of an array in place, and returns a reference to the array.</p>

```javascript
var list = [3, 1, 2];
list.sort();
console.log(list);
// output '1, 2, 3'
```
