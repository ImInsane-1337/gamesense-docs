# type

Returns the type of its only argument, coded as a string. The possible results of this function are `"nil"` (a string, not the value nil), `"number"`, `"string"`, `"boolean"`, `"table"`, `"function"`, `"thread"`, and `"userdata"`.

```typescript
type(value): string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| value | The value to get the type of. | unknown |

Returns `string`
