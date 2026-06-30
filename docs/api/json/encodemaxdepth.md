# json.encode_max_depth

[json.stringify](encodemaxdepth.md) will generate an error when encoding deeply nested JSON once the maximum table depth has been exceeded. This check prevents unnecessarily complicated JSON from slowing down the application, or crashing the application due to lack of process stack space.

By default, [json.stringify](encodemaxdepth.md) will reject JSON with more than 1000 nested tables.

The current setting is always returned, and is only updated when an argument is provided.

```typescript
json.encode_max_depth(depth: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| depth | Must be a positive integer. Default: 1000. | number |

Returns `old_depth: number`
