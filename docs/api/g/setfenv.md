# setfenv

Sets the environment of the given function to the given table.

```typescript
setfenv(stack, env: table): function
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| stack | The function to set the enviroment of. Can also be a number that specifies the function at that stack level: Level 1 is the function calling it. | function |
| env | The new environment of the function. | table |

Returns `function`
