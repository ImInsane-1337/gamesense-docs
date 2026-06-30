# entity.set_prop

Sets the value of the property. For vectors or angles, pass three values.

```typescript
entity.set_prop(ent: number, prop: string, ..., array_index: number)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| ent | Entity index. | number |
| prop | Property name. | string |
| value | The property will be set to this value. | unknown |
| array_index | If propname is an array, the value at this array index will be returned. | number |
