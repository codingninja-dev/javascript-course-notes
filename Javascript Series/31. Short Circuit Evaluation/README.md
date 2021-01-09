<h1 align='center'>~ Short Circuit Evaluation ~</h1>

<p>As logical expressions are evaluated left to right, they are tested for possible "short-circuit" evaluation using the following rules:</p>

<ul>
  <li>false && anything is short-circuit evaluated to false</li>
  <li>true || anything is short-circuit evaluated to true</li>
</ul>

<p>The rules of logic guarantee that these evaluations are always correct. Note that the anything part of the above expressions is not evaluated.</p>

```javascript
false && true  // false
false && '1'   // false
true || false  // true
true || 'Adam' // true
```
