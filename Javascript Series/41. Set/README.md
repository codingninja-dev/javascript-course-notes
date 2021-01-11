<h1 align='center'>~ Set ~</h1>

<p>Set objects are collections of values. You can iterate its elements in insertion order. A value in a Set may only occur once; it is unique in the Set's collection. You can create a new set like below.</p>


```javascript
let mySet = new Set();
```

<h3>Add Value to Set</h3>

```javascript
var list = new Set();
list.add(1);
list.add(2);
list.add(3);
console.log(list);
// output Set { 1, 2, 3 }
```

<h3>Check if Item Exist in Set</h3>

```javascript
var list = new Set();
list.add(1);
list.add(2);
list.add(3);
console.log(list.has(2));
console.log(list.has(4));
// output true, false
```

<h3>Delete Item in Set</h3>

```javascript
var list = new Set();
list.add(1);
list.add(2);
list.add(3);
list.delete(2);
console.log(list);
// output Set { 1, 3 }
```

<h3>Size of Set</h3>

```javascript
var list = new Set();
list.add(1);
list.add(2);
list.add(3);
console.log(list.size);
// output 3
```

<h3>Loop Set</h3>

```javascript
var list = new Set();
list.add(1);
list.add(2);
list.add(3);
for (let item of list) {
  console.log(item);
}
// output 1, 2, 3
```

<h3>Converting between Array and Set</h3>

<p>You can create an Array from a Set using Array.from. Also, the Set constructor accepts an Array to convert in the other direction. Remember that Set objects store unique values. So any duplicate elements from an Array are deleted when converting.</p>

```javascript
var setList = new Set();
var arrayList = Array.from(setList);
var setList = new Set([1, 2, 3, 4]);
```

<h3>Array vs Set</h3>

<ul>
  <li>Deleting Array elements by value is very slow</li>
  <li>Set objects let you delete elements by their value. With an array, you would have to splice based on an element's index</li>
  <li>The value NaN cannot be found with indexOf in an array</li>
  <li>Set objects store unique values. You don't have to manually keep track of duplicates</li>
</ul>
