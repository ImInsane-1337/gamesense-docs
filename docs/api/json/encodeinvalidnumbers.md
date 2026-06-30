# json.encode_invalid_numbers

[json.stringify](encodeinvalidnumbers.md) may generate an error when encoding floating point numbers not supported by the JSON specification such as `Infinity` and `NaN`. This behavior can be changed by calling this function.

Available settings:
`true` - Allow invalid numbers to be encoded. This will generate non-standard JSON, but this output is supported by some libraries.
`false` - Throw an error when attempting to encode invalid numbers. This is the default setting.
`"null"` - Encode invalid numbers as a JSON null value. This allows infinity and NaN to be encoded into valid JSON.

The current setting is always returned, and is only updated when an argument is provided.

```typescript
json.encode_invalid_numbers(setting): boolean
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| setting | The new setting. | unknown |

Returns `old_setting: boolean`
