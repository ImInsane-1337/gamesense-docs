# renderer.gradient

Draws a horizontal or vertical gradient on the screen.

```typescript
renderer.gradient(x: number, y: number, w: number, h: number, r1: number, g1: number, b1: number, a1: number, r2: number, g2: number, b2: number, a2: number, direction: boolean)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | Top left X coordinate | number |
| y | Top left Y coordinate | number |
| w | Width in pixels | number |
| h | Height in pixels | number |
| r1 | Top/Left red color component (0 to 255) | number |
| g1 | Top/Left green color component (0 to 255) | number |
| b1 | Top/Left blue color component (0 to 255) | number |
| a1 | Top/Left alpha (opacity) component (0 to 255) | number |
| r2 | Bottom/Right red color component (0 to 255) | number |
| g2 | Bottom/Right green color component (0 to 255) | number |
| b2 | Bottom/Right blue color component (0 to 255) | number |
| a2 | Bottom/Right alpha (opacity) component (0 to 255) | number |
| direction | Pass true for horizontal (left-to-right) gradient, or false for vertical. | boolean |
