# getfenv

Returns the environment of the function or stack level passed to it.

```typescript
getfenv(stack): table
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| stack | The function to get the enviroment from. Can also be a number that specifies the function at that stack level: Level 1 is the function calling it. | function |

Returns `table`
