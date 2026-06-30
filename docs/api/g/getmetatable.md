# getmetatable

Returns the metatable of the given table if it has one, otherwise returns `nil`. If t does have a metatable, and the `__metatable` metamethod is set, it returns that value instead.

```typescript
getmetatable(tbl: table): table
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tbl | The table to get the metatable from. | table |

Returns `table`
