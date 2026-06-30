# xpcall

Calls the function `func` in "protected mode".
This means that any error inside func is not propagated; instead, `xpcall` catches the error, calls the "error handler" function passed to it, then returns back to the caller. If the first return value is true, the function call succeeded with no errors and the other return values will be the return values from the function. If the first return value is false, the second one will be the error message.

```typescript
xpcall(func, handler, ...): boolean,
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| func | The function to call. | function |
| handler | The error handler function, called when the function fails, called with the error message. You can for example use `client.error_log` to simply log the error to the console | function |
| args | The arguments to pass to `func`. | unknown |

Returns `boolean, result: undefined`
