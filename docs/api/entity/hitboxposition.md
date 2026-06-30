# entity.hitbox_position

Returns world coordinates of the hitboxes, or nil on failure.

```typescript
entity.hitbox_position(player: number, hitbox: number): number, number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| player | The player index. | number |
| hitbox | The hitbox index. Alternatively, a hitbox name (string) can be used. | number |

Returns `x: number, y: number, z: number`
