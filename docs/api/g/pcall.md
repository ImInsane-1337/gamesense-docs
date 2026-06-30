# pcall

Calls the function `func` in "protected mode".
This means that any error inside func is not propagated; instead, pcall catches the error and returns back to the caller. If the first return value is true, the function call succeeded with no errors and the other return values will be the return values from the function. If the first return value is false, the second one will be the error message.

```typescript
pcall(func, ...): boolean,
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| func | The function to call. | function |
| args | The arguments to pass to `func`. | unknown |

Returns `boolean, result: undefined`
