# Chapter 7 - Unit Testing

```javascript
import {expect} from 'chai'

describe("Example Unit Tests", function()
{
	it("Test #A", function()
	{
		function add(a: number, b: number)
		{
			return a + b;
		}
		
		expect(add(3,4)).to.equal(7);
	});
	
	it("Test #B", function()
	{
		function capitalize(value: string)
		{
			var firstChar = value.substring(0,1).toUpperCase();
			var otherChars = value.substring(1);
			var result = firstChar + otherChars;
			return result;
		}
		
		// Answer 1...
	});
	
	it("Test #C", function()
	{
		function validateNumber(value: number, min: number, max: number): boolean
		{
			var validationResult = false;
			
			if (max < min)
			{
				throw new Error("max cannot be less than min");
			}
			else if (min > max)
			{
				throw new Error("min cannot be greater than max");
			}
			else
			{
				validationResult = (value >= min && value <= max);
			}
			
			return validationResult;
		}
		
		// Answer 2...
	});
});
```

---

### What `expect` statements would be required in 'test #B' to ensure that the 'capitalize' function works correctly?

```javascript
expect(result).to.be.a('string');
expect(result.substring(0,1)).to.match(/^[^a-z]$/);
```

---

### What 'expect' statements would be required in 'test #C' to ensure that the 'validateNumber' function works correctly?

**General:**

```javascript
expect(result).to.be.a('boolean');
```
\
**Valid:**

```javascript
expect(result).to.be.true;
```

\
**Invalid:**

```javascript
expect(result).to.be.false;
```
\
Also, the function throws errors for invalid input so mocha/chai should flag them automatically.

**NOTE:** I have worked with Mocha/Chai extensively on a previous project. It is impractical to write full, robust test cases inside a form. If you want me to write unit tests for specific functions or demonstrate past experience, we can discuss it further.

---

**Previous:** [6 - Classes](./6-classes.md)  
**Next:** [8 - Angular](./8-angular.md)

[Contents](./readme.md)