# rawget

Gets the raw value of a table field, without invoking any `__index` metamethod.

```typescript
rawget(tbl: table, key):
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tbl | The table to get the field from. | table |
| key | The key to get from the table. | unknown |

Returns `value: undefined`
