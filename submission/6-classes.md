# Chapter 6 - Classes

```javascript
class Person
{
	constructor(private name: string) {}
	
	sayHello
	{
		console.log(`Hello, my name is ${this.name}`);
	}
}


const person = new Person('John');
```

---

### What would be the expected output of `person.sayHello();`

"Hello, my name is John"

---

### How is it possible that `this.name` is accessible in the `sayHello` method?

The reason that the 'name' property is accessible within the `sayHello` method is because the property is within the scope of the class and its derived objects. The class properties and methods are all within the same scope so they are able to access one another.

In this case, the 'name' property is used by the `sayHello` method in order to incorporate the person's name into the hello message.

---

### After having created a new Person object called 'person', would it be possible to access the class variable 'name' like this `person.name`?

No, it would not be possible to access the 'name' property from the class object by itself. This is because the property is private - It can only be accessed within the class itself and cannot be publicly accessed from the outside (see previous answer).

In order for 'name' to be accessible, the property would have to be public, or at least  use a `get` syntax so that the name can be read, but not changed.

---

### Can you provide a brief description of the difference between 'Composition' and 'Inheritance' in classes?

Inheritance defines the parent-child relationship between different objects in a system. This starts with a superclass that has the base properties, methods, etc. The superclass expands into subclasses which inherit the parent functionality while having unique functionality of their own. For example, a superclass may be a 'Vehicle' while it's subclasses may include 'Car', 'Bike', etc.

Composition is when the whole object is assembled from a series of parts, or sub-objects if you prefer. While inheritance implies a strict hierarchy between objects, composition is less formal with the different parts coming together in order to form a complete package. For example, a 'Car' object is a car in itself but it is also made up of different separate parts such as the engine, brakes, wheels, and so on. What is interesting is that these individual parts - in turn - may be made up from parts themselves. It all depends on how far you want to break it down.

---

[Return to Index](../readme.md)
