# Objects vs. JSON and Summary

## Key Differences Between Objects and JSON

| Feature            | JavaScript Object                  | JSON                          |
| ------------------ | ---------------------------------- | ----------------------------- |
| **Type**           | A real object in memory            | A string (text)               |
| **Key quotes**     | Optional (`name` or `"name"`)      | Required (`"name"`)           |
| **String quotes**  | Single or double quotes            | Double quotes only            |
| **Functions**      | Allowed                            | Not allowed                   |
| **Comments**       | Allowed                            | Not allowed                   |
| **Trailing comma** | Allowed                            | Not allowed                   |
| **Use**            | Working with data in your code     | Sending/storing data as text  |

## Summary

- **Objects** store related data as key-value pairs.
- Use **dot notation** (`obj.key`) or **bracket notation** (`obj["key"]`) to access properties.
- **Methods** are functions inside objects, and `this` refers to the object.
- **JSON** is a text format that looks like an object but is actually a string.
- Use **`JSON.stringify()`** to turn an object into JSON.
- Use **`JSON.parse()`** to turn JSON into an object.

> **Remember:** An object lives in your code, while JSON is text used to share data. They look similar but are not the same thing!

---

**Previous:** [Converting Between Objects and JSON](09-converting-between-objects-and-json.md)

[Back to start](README.md)
