# renderer.circle

Draws a filled circle on the screen

```typescript
renderer.circle(x: number, y: number, r: number, g: number, b: number, a: number, radius: number, start_degrees: number, percentage: number)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | X center position | number |
| y | Y center position | number |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| a | Alpha (opacity) component (0 to 255) | number |
| radius | Radius of the circle in pixels. | number |
| start_degrees | 0 is the right side, 90 is the bottom, 180 is the left, 270 is the top. | number |
| percentage | Must be within [0.0-1.0]. 1.0 is a full circle, 0.5 is a half circle, etc. | number |
