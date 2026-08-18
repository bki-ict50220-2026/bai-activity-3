# Nested Objects

Objects can contain other objects as values.

```javascript
const student = {
  name: "Bob",
  grades: {
    math: 90,
    science: 85,
    english: 78
  }
};

console.log(student.grades.math); // 90
console.log(student["grades"]["science"]); // 85
```

---

**Previous:** [Looping Through Objects](06-looping-through-objects.md)

**Next:** [What is JSON?](08-what-is-json.md)
