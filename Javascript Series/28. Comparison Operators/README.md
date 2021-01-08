<h1 align='center'>~ Comparison Operators ~</h1>

<p>A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically. The sole exceptions to type conversion within comparisons involve the === and !== operators, which perform strict equality and inequality comparisons. These operators do not attempt to convert the operands to compatible types before checking equality. </p>

<table align="center">
  <thead>
    <tr align="center">
      <td><b>Operator</b></td>
      <td><b>Description</b></td>
      <td><b>Examples Returning True</b></td>
    </tr>
  </thead>
  <tbody>
    <tr align="center">
      <td>Equal (==)</td>
      <td>Returns true if the operands are equal.</td>
      <td>3 == '3' or 3 == 3</td>
    </tr>
    <tr align="center">
      <td>Not equal (!=)</td>
      <td>Returns true if the operands are not equal.</td>
      <td>2 == '3' or 1 != 2</td>
    </tr>
    <tr align="center">
      <td>Strict equal (===)</td>
      <td>Returns true if the operands are equal and of the same type.</td>
      <td>3 === 3 or 'a' === 'a'</td>
    </tr>
    <tr align="center">
      <td>Strict not equal (!==)</td>
      <td>Returns true if the operands are of the same type but not equal, or are of different type.</td>
      <td>3 === 2 or 'a' !== 'b'</td>
    </tr>
    <tr align="center">
      <td>Greater than (>)</td>
      <td>Returns true if the left operand is greater than the right operand.</td>
      <td>4 > 2 or 1 > 0</td>
    </tr>
    <tr align="center">
      <td>Greater than or equal (>=)</td>
      <td>Returns true if the left operand is greater than or equal to the right operand.</td>
      <td>5 >= 5 or 2 >= 1</td>
    </tr>
    <tr align="center">
      <td>Less than (<)</td>
      <td>Returns true if the left operand is less than the right operand.</td>
      <td>2 < 3 or 1 < 4</td>
    </tr>
    <tr align="center">
      <td>Less than or equal (<=)</td>
      <td>Returns true if the left operand is less than or equal to the right operand.</td>
      <td>3 <= 3 or 2 <= 4</td>
    </tr>
  </tbody>
</table>
