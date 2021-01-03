<h1 align='center'>~ If Else Statement ~</h1>

<p>The if statement is execute if a statement's logical condition is true. Use the optional else clause to execute a statement if the condition is false.</p>

```javascript
if (true){
  console.log('hello world');
}
// hello world is outputed
```

```javascript
if (true){
  console.log('hello world');
} else {
  console.log('hello');
}
// hello world is outputed
```

```javascript
if (false){
  console.log('hello world');
} else {
  console.log('hello');
}
// hello is outputed
```

<p>If you want to do multiple checks then you can use the else if like below.</p>

```javascript
if (false){
  console.log('hello world');
} else if(true) {
  console.log('hello');
} else {
  console.log('world');
}
// hello is outputed
```

<p>Keep in mind that the below values are evaluated as false. Everything else is evaluated as true.</p>

<ul>
  <li>false</li>
  <li>undefined</li>
  <li>null</li>
  <li>0</li>
  <li>NaN (Not a Number)</li>
  <li>'' (Empty String)</li>
</ul>
