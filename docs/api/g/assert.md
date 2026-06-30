# assert

If the the first argument is `false` or `nil`, an error is thrown with the second argument as the message. Otherwise all the arguments are returned.

```typescript
assert(expression, message: string)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| expression | If this is `false` or `nil`, an error is thrown. | unknown |
| message | The error message to throw. | string |
