# Local Storage (Add, Update, Delete)

## What is Local Storage?

Local Storage is a small storage area that lives **inside the user's browser**. It lets you save data so it survives page refreshes and closing the browser.

- It stores data as **key-value pairs** (a name → a value).
- It belongs to **one website** (one "origin") — other sites cannot see it.
- It can only store **strings**, so objects must be converted to JSON first.

You already learned how to turn objects into strings (`JSON.stringify`) and back again (`JSON.parse`) — Local Storage uses exactly that idea.

## Add an item — `setItem()`

Use `setItem(key, value)` to **add** a new item:

```javascript
localStorage.setItem("username", "Alex");
//           (key)              (value)
```

- **Key** = the label you look up later.
- **Value** = the data you are saving.

> **Important:** Local Storage stores **strings only**. If you save a number, it becomes a string:
>
> ```javascript
> localStorage.setItem("age", 25);
> console.log(typeof localStorage.getItem("age")); // "string" (not "number"!)
> ```

## Read an item — `getItem()`

Use `getItem(key)` to **read** a value back:

```javascript
const name = localStorage.getItem("username");
console.log(name); // "Alex"
```

If the key does not exist, `getItem` returns `null`:

```javascript
console.log(localStorage.getItem("missingKey")); // null (not found)
```

## Update an item — `setItem()` again

To **update** a value, call `setItem` again with the **same key** and a new value:

```javascript
localStorage.setItem("username", "Sam");
console.log(localStorage.getItem("username")); // "Sam"
```

## Delete items — `removeItem()` and `clear()`

Use `removeItem(key)` to **delete** one item:

```javascript
localStorage.removeItem("username");
console.log(localStorage.getItem("username")); // null (not found)
```

Use `clear()` to delete **everything** for the current website:

```javascript
localStorage.clear();
```

## Storing objects in Local Storage

Because Local Storage only stores strings, you must convert an object to JSON to save it, and parse it back to use it:

```javascript
const profile = {
  name: "Alex",
  age: 25,
  isStudent: true
};

// Add — object -> string -> save
localStorage.setItem("profile", JSON.stringify(profile));

// Read — string -> object
const saved = JSON.parse(localStorage.getItem("profile"));
console.log(saved.name); // "Alex"

// Update — change the object, then save it again
saved.age = 26;
localStorage.setItem("profile", JSON.stringify(saved));

// Delete
localStorage.removeItem("profile");
```

> **Remember the pair:**
> - Saving an object → `JSON.stringify()` (object → string)
> - Reading an object → `JSON.parse()` (string → object)

## Quick reference

| Action       | Method                                     |
| ------------ | ------------------------------------------ |
| Add          | `localStorage.setItem(key, value)`         |
| Read         | `localStorage.getItem(key)`                |
| Update       | `localStorage.setItem(key, newValue)`      |
| Delete one   | `localStorage.removeItem(key)`             |
| Delete all   | `localStorage.clear()`                     |

---

**Previous:** [Converting Between Objects and JSON](09-converting-between-objects-and-json.md)

**Next:** [Objects vs. JSON and Summary](11-objects-vs-json-summary.md)
