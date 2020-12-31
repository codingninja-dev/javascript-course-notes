<h1 align='center'>~ Basic Syntax and Comment ~</h1>

<p>To store information you will need to use the var keyword follow by a name you want to give for the data you are storing. Below are a few examples of basic syntax on storing data.</p>

```javascript
var name = 'Adam';   // string
var age = 18;        // number
var canDrive = true; // boolean
```
<p>One thing to keep in mind is that the name you give your variables are case-sensitive. The below example show two different naming which are not the same. So make sure to always remember variable declaration are case sensitive.</p>

```javascript
var firstName = 'Adam';
var firstname = 'Eve';
console.log(firstName); // Adam 
console.log(firstname); // Eve
```

<p>Below can be called a statement. We have a semicolon at the end to distinuguish that this is the end of our statement and we can begin our work on the next statement. If we dint have a semicolon and we have another statement we would get an error.</p>

```javascript
var firstName = 'Adam'; // correct
var firstName = 'Adam' var lastName = 'Smith'; // incorrect
var firstName = 'Adam'; var lastName = 'Smith'; // correct
```

To add comments to your code you can follow the below style to add your comments.

```javascript
// single line comment

/*
 * multi line comment
 */
```
