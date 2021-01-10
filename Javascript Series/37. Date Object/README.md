<h1 align='center'>~ Date Object ~</h1>

<p>JavaScript does not have a date data type. However, you can use the Date object and its methods to work with dates and times in your applications. The Date object has a large number of methods for setting, getting, and manipulating dates. It does not have any properties.</p>

<p>Date1 and Date2 variable is the name of the Date object being created. It can be a new object or a property of an existing object.</p>

```javascript
var date1 = new Date();
var date2 = Date();
console.log(date1);
console.log(date2);
// output for both 'Sun Jan 10 2021 10:47:46 GMT-0800 (Pacific Standard Time)'
```

<h3>Sample of Date Object Usage</h3>

```javascript
var date = new Date("December 25, 2002");
console.log(date);
// output Wed Dec 25 2002 00:00:00 GMT-0800 (Pacific Standard Time)
```

```javascript
var date = new Date(2003, 11, 25);
console.log(date);
// output Thu Dec 25 2003 00:00:00 GMT-0800 (Pacific Standard Time)
```

```javascript
var date = new Date(2005, 11, 25, 9, 30, 0);
console.log(date);
//output Sun Dec 25 2005 09:30:00 GMT-0800 (Pacific Standard Time)
```

<h3>Methods of the Date object</h3>

<p>The Date object methods for handling dates and times fall into these broad categories:</p>

<ul>
  <li>"set" methods, for setting date and time values in Date objects</li>
  <li>"get" methods, for getting date and time values from Date objects</li>
  <li>"to" methods, for returning string values from Date objects</li>
  <li>parse and UTC methods, for parsing Date strings</li>
</ul>

<p>With the "get" and "set" methods you can get and set seconds, minutes, hours, day of the month, day of the week, months, and years separately. These methods use integers to represent these values as follows:</p>

<ul>
  <li>Seconds and minutes: 0 to 59</li>
  <li>Hours: 0 to 23</li>
  <li>Day: 0 (Sunday) to 6 (Saturday)</li>
  <li>Date: 1 to 31 (day of the month)</li>
  <li>Months: 0 (January) to 11 (December)</li>
  <li>Year: years since 1900</li>
</ul>
