# entity.get_bounding_box

Returns the 2D bounding box and alpha multiplier (dormant esp). The contents of x1, y1, x2, y2 must be ignored when alpha_multiplier is zero, which indicates that the bounding box is invalid and should not be drawn.

```typescript
entity.get_bounding_box(ent: number): number, number, number, number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| ent | Player entity index. | number |

Returns `x1: number, y1: number, x2: number, y2: number, alpha_multiplier: number`
