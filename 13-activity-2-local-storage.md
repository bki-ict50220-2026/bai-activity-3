# Activity 2: Store Your Object in Local Storage

Now let's save an object so it survives refreshes. Open the [**eval sandbox site**](https://javascript-is-eval.pages.dev/) and practice putting an object into Local Storage and getting it back out.

**You'll practice:** creating an object, `JSON.stringify`, `localStorage.setItem`, `localStorage.getItem`, and `JSON.parse`.

> **Eval sandbox reminder:** In the eval sandbox, `console.log(...)` prints to the right pane, and `return <value>` prints the returned value. Put `return` at the very end so your earlier `console.log` calls still run.

> **Tip:** Local Storage remembers between runs. If you want a clean start each time, add `localStorage.clear();` as your first line.

## Steps

1. Create an object called `player` with at least 4 properties (for example, `name`, `level`, `score`, and `isOnline`).
2. Use `JSON.stringify` to convert `player` into a JSON string and store it in Local Storage with `localStorage.setItem("player", ...)`.
3. Use `localStorage.getItem("player")` to get the JSON string back out, then use `JSON.parse` to turn it back into an object. Store it in a variable called `saved`.
4. `console.log` the JSON string and the parsed object.
5. `console.log` one property from the parsed object using dot notation.
6. `return` the parsed object.

## Check Your Work

The right pane should show something like:

```
{"name":"Mia","level":3,"score":1200,"isOnline":true}
{ name: "Mia", level: 3, score: 1200, isOnline: true }
Mia
```

<details>
<summary>Need help? Show an example solution</summary>

```javascript
const player = {
  name: "Mia",
  level: 3,
  score: 1200,
  isOnline: true
};

// Store it (object -> JSON string -> Local Storage)
const json = JSON.stringify(player);
localStorage.setItem("player", json);

// Get it back out (Local Storage -> JSON string -> object)
const saved = JSON.parse(localStorage.getItem("player"));

console.log(json);
console.log(saved);
console.log(saved.name);

return saved;
```

</details>

---

**Previous:** [Activity 1: Make Your Own Object](12-activity-1-your-own-object.md)

[Back to start](README.md)
