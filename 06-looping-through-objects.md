# Looping Through Objects

To go through every property in an object, use a `for...in` loop.

```javascript
const fruit = {
  name: "Apple",
  color: "Red",
  price: 1.5
};

for (const key in fruit) {
  console.log(key + ": " + fruit[key]);
}

// name: Apple
// color: Red
// price: 1.5
```

---

**Previous:** [Methods](05-methods.md)

**Next:** [Nested Objects](07-nested-objects.md)
