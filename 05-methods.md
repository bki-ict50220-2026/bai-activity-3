# Methods (Functions Inside Objects)

When a function is stored inside an object, it is called a **method**.

```javascript
const dog = {
  name: "Rex",
  bark: function () {
    console.log("Woof woof!");
  },
  introduce: function () {
    console.log("My name is " + this.name);
  }
};

dog.bark();      // "Woof woof!"
dog.introduce(); // "My name is Rex"
```

> **Tip:** The `this` keyword refers to the object the method belongs to (in this case, `dog`).

---

**Previous:** [Adding, Changing, and Deleting Properties](04-adding-changing-and-deleting-properties.md)

**Next:** [Looping Through Objects](06-looping-through-objects.md)
