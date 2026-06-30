# select

Returns all the arguments passed to it after the index.
Alternatively, if the string `"#"` is passed as the first argument, it returns the total number of arguments passed to it (including `nil`s).

```typescript
select(index: number, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| index | The index of the first element, or alternatively the string `"#"`.` | number |
| args | The arguments to select from. | unknown |
