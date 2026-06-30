# client.find_signature

Finds the specified pattern and returns a pointer to it, or nil if not found.

```typescript
client.find_signature(module_name: string, pattern: string): userdata
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| module_name | Filename of the module that contains the interface | string |
| pattern | String of the signature. Escape with `\x`, replace wildcards with `\xCC`. | string |

Returns `match: userdata`
