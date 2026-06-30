# json.parse

Parses a UTF-8 JSON string into a Lua object (table, number, string, etc).

UTF-16 and UTF-32 JSON strings are not supported.
All escape codes will be decoded and other bytes will be passed transparently.
JSON `null` will be converted to a NULL `lightuserdata` value. This can be compared with `json.null` for convenience.

By default, numbers incompatible with the JSON specification (`infinity`, `NaN`, hexadecimal) can be parsed. This default can be changed with [json.decode_invalid_numbers](parse.md).

```typescript
json.parse(json_text: string):
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| json_text | The JSON string to parse. | string |

Returns `object: undefined`
