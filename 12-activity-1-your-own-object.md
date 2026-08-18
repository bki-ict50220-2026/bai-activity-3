# Activity 1: Make Your Own Object

Now it's your turn. Open the [**eval sandbox site**](https://javascript-is-eval.pages.dev/) and build your own object from scratch.

**You'll practice:** creating an object with existing properties, then adding new properties to it.

> **Eval sandbox reminder:** In the eval sandbox, `console.log(...)` prints to the right pane, and `return <value>` prints the returned value. Put `return` at the very end so your earlier `console.log` calls still run.

## Steps

1. Create an object called `profile` with **at least 4 existing properties** about a person. Mix data types — try a string, a number, and a boolean.
2. Use `console.log` to print the whole object.
3. Use `console.log` and **dot notation** to print two of the existing properties on their own.
4. **Add** two new properties to the object (for example, a `city` and a `country`).
5. Use `console.log` to print the object again and check the new properties are there.
6. `return` the finished object at the end.

## Check Your Work

The right pane should show something like:

```
{ name: "Alex", age: 25, isStudent: true, hobby: "painting" }
Alex
25
{ name: "Alex", age: 25, isStudent: true, hobby: "painting", city: "Sydney", country: "Australia" }
```

<details>
<summary>Need help? Show an example solution</summary>

```javascript
const profile = {
  name: "Alex",
  age: 25,
  isStudent: true,
  hobby: "painting"
};

console.log(profile);
console.log(profile.name);
console.log(profile.age);

profile.city = "Sydney";      // add
profile.country = "Australia"; // add

console.log(profile);

return profile;
```

</details>

---

**Previous:** [Objects vs. JSON and Summary](11-objects-vs-json-summary.md)

**Next:** [Activity 2: Store Your Object in Local Storage](13-activity-2-local-storage.md)
