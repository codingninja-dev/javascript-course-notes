<h1 align='center'>~ For Of Loop ~</h1>

<p>For of loop is used to iterate over iterable objects (including Array, Map, Set, arguments object and so on).</p>

```javascript
var number = [1,2,3,4];

for(var item of number) {
  console.log(item);
}
// output 1,2,3,4
```

```javascript
var name = 'Adam';

for(var item of name) {
  console.log(item);
}
// output 'A','d','a','m'
```
