<h1 align='center'>~ Literals ~</h1>

<p>Literal in javascript represents value or fixed value.</p>

```javascript
var number = 5; // 5 represents a literal in javascript
```

<p>There are seven types of literal in javascript.</p>

<ul>
  <li>Array</li>
  <li>Boolean</li>
  <li>Floating-point</li>
  <li>Numeric</li>
  <li>Object</li>
  <li>RegExp</li>
  <li>String</li>
</ul>

<h3>Array</h3>
<p>An array literal is a list of zero or more values which represents an array element. When you create an array using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified.</p>

```javascript
var coffees = ['French Roast', 'Colombian', 'Kona'];
```

<h3>Boolean</h3>
<p>The Boolean type has two literal values: true and false.</p>

```javascript
var switch = true;
var switch = false;
```

<h3>Floating-point</h3>
<p>A floating-point literal can have the following parts:</p>
<ul>
  <li>A decimal integer which can be signed (preceded by "+" or "-")</li>
  <li>A decimal point (".")</li>
  <li>A fraction (another decimal number)</li>
  <li>An exponent</li>
</ul>

```javascript
var number = 4.64;
var number = -2.34;
var number = -1.2E+4;
```

<h3>Numeric</h3>
<p>Number and BigInt types can be written in decimal (base 10), hexadecimal (base 16), octal (base 8) and binary (base 2)</p>
<ul>
  <li><b>Decimal Numeric Literal</b> - is a sequence of digits without a leading 0 (zero).</li>
  <li><b>Octal Literal</b> - A leading 0 (zero) on a numeric literal, or a leading 0o (or 0O). Can include only the digits 0–7.</li>
  <li><b>Hexadecimal Literal</b> - A leading 0x (or 0X). It can include digits (0–9) and the letters a–f and A–F. (The case of a character does not change its value. Therefore: 0xa = 0xA = 10 and 0xf = 0xF = 15.)</li>
  <li><b>Binary Literal</b> - A leading 0b (or 0B). It can only include the digits 0 and 1.</li>
</ul>


```javascript
var number = 117;    // (decimal, base 10)
var number = 015;    // (octal, base 8)
var number = 0x1123; // (hexadecimal, "hex" or base 16)
var number = 0b0011; // (binary, base 2)
```

<h3>Object</h3>
<p>An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces {}.</p>

```javascript
var person = { name : 'Adam', age : 18, favoriteNumber : 3 };
```

<h3>RegExp</h3>
<p>A regex literal is a pattern enclosed between slashes. The following is an example of a regex literal. A regex literal is used in search functions to quickly find a pattern within the searched term.</p>

```javascript
var re = /ab+c/;
```

<h3>String</h3>
<p>A string literal is zero or more characters enclosed in double (") or single (') quotation marks.</p>

```javascript
var word = 'welcome';
var word = "goodbye";
```
