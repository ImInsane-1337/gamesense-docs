# tostring

Receives an argument of any type and converts it to a string in a reasonable format. For complete control of how numbers are converted, use `string.format`. If the metatable of `value` has a `__tostring` metamethod, then it will be called with `value` as the only argument and will return the result.

```typescript
tostring(value): string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| value | The value to convert to a string. | unknown |

Returns `string`
