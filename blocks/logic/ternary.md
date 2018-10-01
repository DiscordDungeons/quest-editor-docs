# Ternary Block

![Ternary Block](images/ternary.jpg)

The ternary block returns the value of `expr1` if `condition` is `true`, otherwise, it returns the value of `expr2`.

To specify the condition, attach a condition block to the `test` input.

To specify the return value if the condition is true, attach it to the `if true` input.

To specify the return value if the condition is false, attach it to the `if false` input.

### Generated Code

```js
condition ? if_true : if_false;
```
