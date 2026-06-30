# json.stringify

Serializes a Lua object into a JSON string.

It supports the following types:
`boolean`, `nil`, `number`, `string`, `table`

The remaining Lua types will generate an error:
`function`,  `lightuserdata`, `thread`, `userdata`

By default, numbers are encoded with 14 significant digits. Refer to [json.encode_number_precision](stringify.md) for details.

!!!warning
This function will successfully encode/decode binary strings, but this is technically not supported by JSON and may not be compatible with other JSON libraries. To ensure the output is valid JSON, applications should ensure all Lua strings passed to `json.stringify` are UTF-8.
Base64 is commonly used to encode binary data as the most efficient encoding under UTF-8 can only reduce the encoded size by a further ~8%.
!!!

```typescript
json.stringify(object): string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| object | The Lua object to serialize. | unknown |

Returns `string`
