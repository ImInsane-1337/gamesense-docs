# entity.get_prop

Returns the value of the property, or nil on failure. For vectors or angles, this returns three values.

```typescript
entity.get_prop(ent: number, prop: string, array_index: number):
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| ent | Entity index. | number |
| prop | Property name. | string |
| array_index | If propname is an array, the value at this array index will be returned. | number |

Returns `netprop value: undefined`
