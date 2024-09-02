## Type Conversion (Manually)

https://zh.javascript.info/type-conversions

```javascript
const birthYear = "1997";

// Type conversion (Manually)
console.log(Number(birthYear));
console.log(birthYear);
console.log(Number(birthYear) + 18);

// Type conversion can't change the original value type
console.log(birthYear + 18);

console.log(Boolean({})); //true
console.log(Boolean(0)); //false

```

## Type Coercion (Automatic)
```javascript
// Same input due to type coercion
console.log("I'm " + 23 + " years old.");
console.log("I'm " + "23" + " years old.");
```
