<h1 align='center'>~ For In Loop ~</h1>

<p>The for...in statement iterates a specified variable over all the enumerable properties of an object. For each distinct property, JavaScript executes the specified statements.</p>

```javascript
var person = { name : 'Adam', age : 12, phoneNumber : '626-234-1241'};

for(var item in person) {
  console.log(item);
}
// output name, age, phoneNumber
```

```javascript
var person = { name : 'Adam', age : 12, phoneNumber : '626-234-1241'};

for(var item in person) {
  console.log(person[item]);
}
// output 'Adam', 12, '626-234-1241'
```

<p>When the loop is executed the item variable gets stored the key of the object. Object is comprised of key value pairs. In the first property of the object the 'name' is the key and 'Adam' is the value.</p>
