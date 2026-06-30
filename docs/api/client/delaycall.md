# client.delay_call

Executes the callback after delay seconds, passing the arguments to it.

```typescript
client.delay_call(delay: number, callback, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| delay | Time in seconds to wait before calling callback. | number |
| callback | The lua function that will be called after delay seconds. | function |
| args | Arguments that will be passed to the callback. | unknown |
