# renderer.world_to_screen

Returns the screen coordinates of a world position or nil if the world position is not visible on your screen.

```typescript
renderer.world_to_screen(x: number, y: number, z: number): number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | X position in the world | number |
| y | Y position in the world | number |
| z | Z position in the world | number |

Returns `x: number, y: number`
