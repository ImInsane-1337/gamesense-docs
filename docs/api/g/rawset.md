# rawset

Sets the raw value of a table field, without invoking any `__newindex` metamethod.

```typescript
rawset(tbl: table, key, value)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tbl | The table to modify. | table |
| key | The key to set on the table. | unknown |
| value | The value to set the table key to. | unknown |
