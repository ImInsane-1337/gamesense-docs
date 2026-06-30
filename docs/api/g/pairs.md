# pairs

Returns three values: an iterator function, the table `tbl` and `nil`. Each time the iterator function is called, it returns the next *key-value pair* in the table.

When used in a generic for-in-loop, the return values can be used to iterate over all key-value pairs in the table.
The iteration order is not specified and tables do not keep their insertion order.

```typescript
pairs(tbl: table): function, table, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tbl | The array-like table to iterate over. | table |

Returns `function, table, number`
