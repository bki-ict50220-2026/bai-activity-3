# Adding, Changing, and Deleting Properties

## Adding and Changing Properties

You can add a new property or change an existing one with the assignment operator (`=`).

```javascript
const book = {
  title: "JavaScript Basics"
};

// Adding a new property
book.author = "Jane Doe";
book.pages = 250;

// Changing an existing property
book.title = "Advanced JavaScript";

console.log(book);
// { title: "Advanced JavaScript", author: "Jane Doe", pages: 250 }
```

## Deleting Properties

Use the `delete` keyword to remove a property.

```javascript
const book = {
  title: "JavaScript Basics",
  author: "Jane Doe",
  pages: 250
};

delete book.pages;

console.log(book);
// { title: "JavaScript Basics", author: "Jane Doe" }
```

---

**Previous:** [Accessing Properties](03-accessing-properties.md)

**Next:** [Methods](05-methods.md)
