## Type conversion(类型转换)

```javascript
const birthYear = "1997";

// Type conversion (Manually)
console.log(Number(birthYear));
console.log(birthYear);
console.log(Number(birthYear) + 18);

// Type conversion can't change the original value type
console.log(birthYear + 18);

## Type Coercion (Automatic)
//Same input due to type Coercion
console.log("I'm " + 23 + " years old.");
console.log("I'm " + "23" + " years old.");
