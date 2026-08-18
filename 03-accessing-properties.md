# Accessing Properties

There are two ways to read a value from an object.

## Dot Notation

```javascript
const person = {
  name: "Alice",
  age: 30
};

console.log(person.name); // "Alice"
console.log(person.age);  // 30
```

## Bracket Notation

```javascript
console.log(person["name"]); // "Alice"
console.log(person["age"]);  // 30
```

> **Tip:** Use bracket notation when the key name has spaces, special characters, or is stored in a variable.

```javascript
const key = "name";
console.log(person[key]); // "Alice"
```

---

**Previous:** [Creating Objects](02-creating-objects.md)

**Next:** [Adding, Changing, and Deleting Properties](04-adding-changing-and-deleting-properties.md)
