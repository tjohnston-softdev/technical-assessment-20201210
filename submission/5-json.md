# Chapter 5 - JSON

```javascript
const data =
[
	{id: 1, name: 'John', email: 'john@example.com', favoriteColor: 'Green'},
	{id: 2, name: 'Sarah', email: 'sarah@example.com', favoriteColor: 'Blue'},
	{id: 3, name: 'Bill', email: 'bill@example.com', favoriteColor: 'Red'},
	{id: 4, name: 'Jen', email: 'jen@example.com', favoriteColor: 'Blue'},
];
```

---

### Write a single line of JavaScript code that will extract all the email addresses from 'data' into an array.

```javascript
var emailAddresses = data.map(function(obj)
{
	return obj.email;
});
```

---

### Write a single line of JavaScript code to extract all the objects where the 'favoriteColor' is 'Blue' into an array

```javascript
var blueList = data.filter(function (obj)
{
	return (obj.favoriteColor === "Blue");
});
```

---

[Return to Index](../readme.md)
