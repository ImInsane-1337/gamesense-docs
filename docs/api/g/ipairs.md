# ipairs

Returns three values: an iterator function, the table `tbl` and the number `0`. Each time the iterator function is called, it returns the next *numerical index-value pair* in the table.

When used in a generic for-in-loop, the return values can be used to iterate over each numerical index in the table.

```typescript
ipairs(tbl: table): function, table, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tbl | The array-like table to iterate over. | table |

Returns `function, table, number`
