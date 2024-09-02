## Type conversion and Coercion(类型转换和强制转换)

```javascript
const birthYear = "1997";
// Type conversion
console.log(Number(birthYear));
console.log(birthYear);
console.log(Number(birthYear) + 18);
// Type conversion can't change the original value type
console.log(birthYear + 18);
