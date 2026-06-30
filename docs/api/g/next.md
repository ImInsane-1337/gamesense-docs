# next

Returns the first key/value pair in the `t` table. If a key argument was specified then returns the next element in the table based on the key provided.

If the table is empty or the specified key was the last key in the array, it returns nil. This means that you can use `next(t)` to check whether a table is empty.

The order in which the indices are enumerated is not specified, even for numeric indices. To traverse an array-like table in order, use a numerical for loop or [ipairs](ipairs.md).

```typescript
next(t: table, key: any): , value
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| t | The table to traverse. | table |
| key | The key to use as the start point for the traversal. If absent, the traversal starts at the first key in the table. | any |

Returns `next_key: undefined, value`
