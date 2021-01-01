<h1 align='center'>~ Data Types ~</h1>

<p>There are two kinds of data type. There are primitive and non-primitive data types when storing data in variable.</p>

<ul>
  <li>Primitive Data Types (String, Number, Boolean, Undefined, and Null)</li>
  <li>Non-Primitive Data Types (Objects and Arrays)</li>
</ul>

<h3>Primitive Data Types</h3>

<ul>
  <li>String ('a', 'cookie', etc)</li>
  <li>Number (1, 2, 3, etc)</li>
  <li>Boolean (true, false, 1, 0)</li>
  <li>Undefined (undefined)</li>
  <li>Null (null)</li>
</ul>

<h3>Non-Primitive Data Types</h3>

<ul>
  <li>Objects ({name : 'Adam', age : 34})</li>
  <li>Arrays ([1,2,3], [[1,2], [3,4]])</li>
</ul>

<h3>Type Coercion in Javascript</h3>

<p>Type coercion is the automatic or implicit conversion of values from one data type to another data type(eg. string to number & vice-versa). Type conversion is similar to Type Coercion because they both convert values from one data type to another with one key difference — type coercion is implicit whereas type conversion can be either implicit or explicit.
In simple terms, we as a developer don't explicitly perform type coercion. It is done internally by the javascript engine.</p>

```javascript
console.log(5 + '5'); // '55'
```

<p>In other languages this would be a compiler issue when doing math operations on different data types. However, since javascript is a dynamic language it will internally tries to make things even by making both the operands of the same type. So the above the number 5 would be coerce to a string type to be combined with the other string 5. Type Coercion is something to always keep in mind and understand when working with the Javascript language.</p>

