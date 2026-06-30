# client.trace_line

Returns fraction, entindex. fraction is a percentage in the range [0.0, 1.0] that tells you how far the trace went before hitting something, so 1.0 means nothing was hit. entindex is the entity index that hit, or -1 if no entity was hit.

```typescript
client.trace_line(skip_entindex: number, from_x: number, from_y: number, from_z: number, to_x: number, to_y: number, to_z: number): number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| skip_entindex | Ignore this entity while tracing | number |
| from_x | X coordinate of the start of the trace | number |
| from_y | Y coordinate of the start of the trace | number |
| from_z | Z coordinate of the start of the trace | number |
| to_x | X coordinate of the end of the trace | number |
| to_y | Y coordinate of the end of the trace | number |
| to_z | Z coordinate of the end of the trace | number |

Returns `fraction: number, entindex: number`
