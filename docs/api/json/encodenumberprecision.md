# json.encode_number_precision

The amount of significant digits returned by [json.stringify](encodenumberprecision.md) when encoding numbers can be changed to balance accuracy versus performance. For data structures containing many numbers, setting json.encode_number_precision to a smaller integer, for example 3, can improve encoding performance by up to 50%.
By default, Lua CJSON will output 14 significant digits when converting a number to text.

The current setting is always returned, and is only updated when an argument is provided.

```typescript
json.encode_number_precision(precision: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| precision | Must be a positive integer. Default: 14. | number |

Returns `old_precision: number`
