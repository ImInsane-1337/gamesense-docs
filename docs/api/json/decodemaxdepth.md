# json.decode_max_depth

[json.parse](decodemaxdepth.md) will generate an error when parsing deeply nested JSON once the maximum array/object depth has been exceeded. This check prevents unnecessarily complicated JSON from slowing down the application, or crashing the application due to lack of process stack space.

An error may be generated before the depth limit is hit if Lua is unable to allocate more objects on the Lua stack.
By default, [json.parse](decodemaxdepth.md) will reject JSON with arrays and/or objects nested more than 1000 levels deep.

The current setting is always returned, and is only updated when an argument is provided.

```typescript
json.decode_max_depth(depth: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| depth | Must be a positive integer. Default: 1000. | number |

Returns `old_depth: number`
