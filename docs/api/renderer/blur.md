# renderer.blur
danger
Using this function in a `paint_ui` callback will result in 'too many indices for index buffer' crashes. Calls to this function are not flushed when not in-game, so they eventually pile-up and exceed the limit.

# renderer.blur

Creates a region on the screen that blurs everything behind it.

```typescript
renderer.blur(x: number, y: number, w: number, h: number, alpha: number, amount: number)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | The X coordinate of the rectangle | number |
| y | The Y coordinate of the rectangle | number |
| w | The width of the rectangle | number |
| h | The height of the rectangle | number |
| alpha | The alpha of the blur, in the range of 0.0 to 1.0 | number |
| amount | The amount of blur, in the range of 0.0 to 1.0 | number |
