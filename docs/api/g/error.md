# error

Terminates the last protected function called and outputs message as an error message. If the function containing the error is not called in a protected function (pcall), then the script which called the function will terminate. The error function itself never returns and acts like a script error.
The level argument specifies how to get the error position. With level 1 (the default), the error position is where the error function was called. Level 2 points the error to where the function that called error was called; and so on. Passing a level 0 avoids the addition of error position information to the message.

```typescript
error(message: string, level: number)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| message | The error message to throw. | string |
| level | The stack level of the error. Defaults to 1. | number |
