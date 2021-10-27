# Chapter 8 - Angular

```javascript
/* etc */
@Component(
{
	selector: 'app-home',
	templateUrl: 'home.page.html',
	styleUrls: ['home.page.scss']
})

export class HomePage
{
	
	constructor(private router: Router,
	/* etc */
```

---

### In the Component decorator, what is the `selector` for?

This represents the CSS selector that identifies elements related to this component.

---

### If you wanted to respond to the `OnInit` lifecycle hook for this component, how would you alter the class declaration to allow for this?

Add `implements OnInit` after the class name (HomePage)

---

### What class method would you then need to implement?

`ngOnInit`

---

### If you want to create a service class, what decorator would you use and what options would you provide for it to be accessible to all components using dependency injection in the component constructor?

Not sure.

---

[Return to Index](../readme.md)
