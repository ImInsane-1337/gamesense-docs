# client.draw_debug_text

Draws a DebugOverlay text at the specified 3d position. Avoid calling this during the paint event.

```typescript
client.draw_debug_text(x: number, y: number, z: number, line_offset: number, duration: number, r: number, g: number, b: number, a: number, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | X coordinate | number |
| y | Y coordinate | number |
| z | Z coordinate | number |
| line_offset | Used for vertical alignment, use 0 for the first line. | number |
| duration | Time in seconds that the text will remain on the screen. | number |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| a | Alpha (opacity) component (0 to 255) | number |
| text | The text that will be drawn | unknown |
