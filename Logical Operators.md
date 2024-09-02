## OR "||" finds the first truthy value

```javascript
alert( 1 || 0 ); // 1 (1 is truthy)

alert( null || 1 ); // 1 (1 is the first truthy value)
alert( null || 0 || 1 ); // 1 (the first truthy value)

alert( undefined || null || 0 ); // 0 (all falsy, returns the last value)
```

### Some interesting usage
1. Getting the first truthy value from a list of variables or expressions.

```javascript
let firstName = "";
let lastName = "";
let nickName = "SuperCoder";

alert( firstName || lastName || nickName || "Anonymous"); // SuperCoder
```

2. Short-circuit evaluation.

```javascript
true || alert("not printed");
false || alert("printed");
```

## AND “&&” finds the first falsy value (the same as OR "||")

## Precedence of AND && is higher than OR ||(AND &&的优先级高于 OR ||)

## Examples
### Check the login 检查登录情况
```javascript
const userName = prompt("Please log in!");
if (userName === "Admin") {
  const password = prompt("Enter your password: ");
  if (password === "TheMaster") {
    alert("Welcome!");
 ```
  ```diff
   -//取消输入可以处理为 password === null
  ```javascript
  } else if (password === "" || password === null) {
    alert("Canceled");
  } else {
    alert("Wrong password");
  }
} else if (userName === "" || userName === null) {
  alert("Canceled");
} else {
  alert("I don't know you");
}
```
