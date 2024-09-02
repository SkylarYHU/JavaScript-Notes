## 为什么要用严格相等“===”？

```diff
Notice:
- 不要使用 “==”
+ 永远使用 “===”
```
link: https://zh.javascript.info/comparison

### Loose equality 普通的相等性检查 == 
<p>存在一个问题，因为它会进行类型转换，所以它不能区分出 0 和 false，也同样无法区分空字符串和 false</p>

```javascript
alert( 0 == false ); // true
alert( '' == false ); // true
"2" > "12" → true //基于 Unicode 编码值
```

### Strict equality 严格相等运算符 === 
<p>在进行比较时不会做任何的类型转换，避免犯错</p>
```javascript
alert( 0 === false ); // false，因为被比较值的数据类型不同
```

## 总结
1. 比较运算符始终返回布尔值。
2. 字符串的比较，会按照“词典”顺序逐字符地比较大小。
3. 当对不同类型的值进行比较时，它们会先被转化为数字（不包括严格相等检查）再进行比较。
4. 在非严格相等 == 下，null 和 undefined 相等且各自不等于任何其他的值。
5. 在使用 > 或 < 进行比较时，需要注意变量可能为 null/undefined 的情况。比较好的方法是单独检查变量是否等于 null/undefined。
