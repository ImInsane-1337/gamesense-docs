# setmetatable

Sets the metatable of the given table `tbl` to `metatable`. If `metatable` is nil, the metatable of t is removed. Finally, this function returns the table `tbl` which was passed to it. If `tbl` already has a metatable whose `__metatable` metamethod is set, calling this on `tbl` raises an error.

```typescript
setmetatable(tbl: table, metatable: table)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tbl | The table to set the metatable of. | table |
| metatable | The new metatable | table |
