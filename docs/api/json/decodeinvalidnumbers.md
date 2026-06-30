# json.decode_invalid_numbers

[json.parse](decodeinvalidnumbers.md) may generate an error when trying to decode numbers not supported by the JSON specification. *Invalid numbers* are defined as: infinity, not-a-number (NaN) and hexadecimal

Available settings:
`true` - Accept and decode invalid numbers. This is the default setting.
`false` - Throw an error when invalid numbers are encountered.

The current setting is always returned, and is only updated when an argument is provided.

```typescript
json.decode_invalid_numbers(setting: boolean): boolean
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| setting | The new setting. `true` to accept and decode invalid numbers, `false` to throw an error. | boolean |

Returns `old_setting: boolean`
