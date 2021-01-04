<h1 align='center'>~ Loop Statement ~</h1>

<p>There are two loop statements that are used quite a bit in javascript.</p>

<ul>
  <li>break</li>
  <li>continue</li>
</ul>

<h3>Break Statement</h3>

<p>Use the break statement to terminate a loop or a switch.</p>

```javascript
for(var x = 1 ; x <= 10 ; x++) {
  if(x > 5) {
    break;
  }
  console.log(x);
}
// outputs 1 - 5
```

```javascript
var name = 'adam';
switch(name) {
  case 'adam':
    console.log('Hi Adam!');
    break;
  case 'Eve':
    console.log('Hi Eve!');
    break;
  default:
    console.log('No name found!');
}
// outputs 'Hi Adam!'
```

```javascript
var x = 1;
while(x <= 10) {
  if(x > 5) {
    break;
  }
  console.log(x);
  x++;
}
// outputs 1 - 5
```

```javascript
var x = 0;
do {
  if(x >= 5) {
    break;
  }
  x++;
  console.log(x);
} while(x <= 10);
// outputs 1 - 5
```

<h3>Continue Statement</h3>

<p>The continue statement can be used to restart a for, while, or do-while loop.</p>

```javascript
for(var x = 1 ; x <= 10 ; x++) {
  if(x === 5) {
    continue;
  }
  console.log(x);
}
// outputs 1 - 10 without 5
```

```javascript
var x = 1;
while(x <= 10) {
  if(x === 5) {
    x++;
    continue;
  }
  console.log(x);
  x++;
}
// outputs 1 - 10 without 5
```

```javascript
var x = 0;
do {
  if(x === 4) {
    x++;
    continue;
  }
  x++;
  console.log(x);
} while(x < 10);
// outputs 1 - 10 without 5
```
