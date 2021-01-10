<h1 align='center'>~ Regular Expression ~</h1>

<p>Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects.</p>

These patterns are used with methods from RegExp and String Object.

<table>
  <thead>
    <tr>
      <td><b>RegExp</b></td>
      <td><b>String</b></td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>test(), exec()</td>
      <td>match(), matchAll(), replace(), replaceAll(), search(), split()</td>
    </tr>
  </tbody>
</table>

<p>You construct a regular expression in one of two ways:</p>

<ul>
  <li>regular expression literal</li>
  <li>constructor function of the RegExp object</li>
</ul>

<h3>Regular Expression Literal</h3>

<p>Regular expression literals provide compilation of the regular expression when the script is loaded. If the regular expression remains constant, using this can improve performance.</p>

```javascript
let re = /ab+c/;
```

<h3>Constructor Function of the RegExp object</h3>

<p>Using the constructor function provides runtime compilation of the regular expression. Use the constructor function when you know the regular expression pattern will be changing, or you don't know the pattern and are getting it from another source, such as user input.</p>

```javascript
let re = new RegExp('ab+c');
```

<h3>Examples</h3>

<h4 align="center">RegExp</h4>

<p>The test() method executes a search for a match between a regular expression and a specified string. Returns true or false.</p>

```javascript
// test() method
const sentence = 'I will go with Adam to the library.';
const regex = RegExp('Adam');
console.log(regex.test(sentence));
// output true
```

<p>The exec() method executes a search for a match in a specified string. Returns a result array, or null.</p>

```javascript
// exec() method
const sentence = 'I will go with Adam to the library.';
const regex = RegExp('Adam');
console.log(regex.exec(sentence));
// output ["Adam"] 
```

<h4 align="center">String</h4>

<p>The match() method retrieves the result of matching a string against a regular expression. </p>

```javascript
// match() method
const sentence = 'I will go with Adam to the library.';
const regex = RegExp('Adam');
console.log(sentence.match(regex));
// output ["Adam"] 
```

<p>The matchAll() method returns an iterator of all results matching a string against a regular expression, including capturing groups.</p>

```javascript
// matchAll() method
const sentence = 'I will go with Adam to the library. I think.';
const regex = RegExp('I', 'g');
const matches = sentence.matchAll(regex);

for (const match of matches) {
  console.log(match);
}
// output below
// [
//   'I',
//   index: 0,
//   input: 'I will go with Adam to the library. I think.',
//   groups: undefined
// ]
// [
//   'I',
//   index: 36,
//   input: 'I will go with Adam to the library. I think.',
//   groups: undefined
// ]
```

<p>The replace() method returns a new string with some or all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function to be called for each match. If pattern is a string, only the first occurrence will be replaced. The original string is left unchanged.</p>

```javascript
// replace() method
const sentence = 'I will go with Adam to the library. I think Adam.';
const regex = RegExp('Adam', 'i');
const newSentence = sentence.replace(regex, 'Joe');
console.log(newSentence);
// output 'I will go with Joe to the library. I think Adam.'
```

<p>The replaceAll() method returns a new string with all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function to be called for each match. The original string is left unchanged.</p>

```javascript
// replaceAll() method
const sentence = 'I will go with Adam to the library. I think Adam.';
const regex = RegExp('Adam', 'gi');
const newSentence = sentence.replaceAll(regex, 'Joe');
console.log(newSentence);
// output 'I will go with Joe to the library. I think Joe.'
```

<p>The search() method executes a search for a match between a regular expression and this String object.</p>

```javascript
// search() method
const sentence = 'I will go with Adam to the library. I think Adam.';
const regex = RegExp('Adam', 'gi');
const newSentence = sentence.search('Adam');
console.log(newSentence);
// output 15
```

<p>The split() method divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array.  The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call.  </p>

```javascript
// split() method
const sentence = 'I will go with Adam to the library. I think Adam.';
const regex = RegExp('Adam', 'gi');
const newSentence = sentence.split('Adam');
console.log(newSentence);
// output ["I will go with " , " to the library. I think " , "."] 
```
