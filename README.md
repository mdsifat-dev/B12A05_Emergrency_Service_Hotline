## Live Link

[Click here](https://mdsifat-dev.github.io/B12A05_Emergrency_Service_Hotline/)

### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

- getElementById(): Selects a single element by its unique id attribute. IDs are intended to be unique within an HTML document. Use getElementById() for quick access to a single, uniquely identified element
- getElementsByClassName(): Selects elements based on their class attribute, returning all elements that possess the specified class name. Use getElementsByClassName() when you need a live collection of elements sharing a common class.
- querySelector(): Selects the first element that matches a specified CSS selector (e.g., #id, .class, tagname, or more complex combinations). Use querySelector() when you need the first element matching a CSS selector.
- querySelectorAll(): Selects all elements that match a specified CSS selector. Use querySelectorAll() when you need all elements matching a CSS selector, for more versatile and modern DOM selection.

### 2. How do you create and insert a new element into the DOM?

```javascript
const div = document.createElement('div');
div.textContent = 'Hello World!';
document.body.appendChild(div);
```

- createElement → Makes new element.
- appendChild → pushes into the DOM.

### 3. What is Event Bubbling and how does it work?

- When you click something inside a webpage, the event doesn’t just stay there.
  It starts from the element you clicked → then goes to its parent → then to the parent’s parent → and keeps going up like bubbles in water.

### 4. What is Event Delegation in JavaScript? Why is it useful?

- Event Delegation means instead of adding event listeners to lots of child elements, you put ONE listener on their parent and let event bubbling handle the rest. The parent “catches” the event when it bubbles up, and you check which child triggered it.

**Why is it Useful?**

- Less Code → You don’t need 100 listeners for 100 items.
- Better Performance → One listener instead of many.
- Handles Dynamic Elements → Even if new items are added later, the parent listener still works.

### 5. What is the difference between preventDefault() and stopPropagation() methods?

The preventDefault() and stopPropagation() methods in JavaScript event handling address distinct aspects of event behavior in the Document Object Model (DOM).

- preventDefault(): controls the default action of the event on the target element.
- stopPropagation(): controls the propagation of the event through the DOM hierarchy.
