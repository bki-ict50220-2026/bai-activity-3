# Converting Between Objects and JSON

JavaScript provides two built-in methods to move between objects and JSON.

## 1. `JSON.stringify()` — Object → JSON

This converts a JavaScript object into a JSON string.

```javascript
const person = {
  name: "Alice",
  age: 30
};

const jsonString = JSON.stringify(person);
console.log(jsonString);
// '{"name":"Alice","age":30}'

console.log(typeof jsonString); // "string"
```

## 2. `JSON.parse()` — JSON → Object

This converts a JSON string back into a JavaScript object.

```javascript
const jsonString = '{"name":"Alice","age":30}';

const person = JSON.parse(jsonString);
console.log(person.name); // "Alice"
console.log(person.age);  // 30

console.log(typeof person); // "object"
```

## Round Trip Example

```javascript
// Object → JSON → Object
const original = { city: "Melbourne", population: 5000000 };

const asJson = JSON.stringify(original);   // Convert to JSON string
const asObject = JSON.parse(asJson);       // Convert back to object

console.log(asObject.city); // "Melbourne"
```

---

**Previous:** [What is JSON?](08-what-is-json.md)

**Next:** [Local Storage (Add, Update, Delete)](10-local-storage.md)
