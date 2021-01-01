<h1 align='center'>~ String Parsing ~</h1>

<p>If you want to convert a string to a number explicitly then you can use the below provided by Javascript.</p>

<ul>
  <li>parseInt (without decimal)</li>
  <li>parseFloat (with decimal)</li>
  <li>Unary Plus Operator</li>
</ul>

<h3>parseInt</h3>

```javascript
var number = '100';
var parsedNumber = parseInt(number);
console.log(parsedNumber); // 100 instead of '100'
```

<h3>parseFloat</h3>

```javascript
var number = '100.01';
var parsedNumber = parseFloat(number);
console.log(parsedNumber); // 100.01 instead of '100.01'
```

<h3>Unary Plus Operator</h3>

```javascript
var number = '100';
console.log(+number); // 100 instead of '100'
```

<p>The difference between the unary plus operator and the parseInt function is that the parseInt function allows you to pass in one more parameter to determine the radix.</p>

```javascript
var number = '100';
var parsedNumber = parseInt(number, 10); // type of number system (2 - binary, 10 - decimal)
console.log(parsedNumber); // 100 instead of '100'
```

```javascript
var number = '101';
var parsedNumber = parseInt(number, 2);
console.log(parsedNumber); // 5 instead of '101'
```
