# renderer.text

Draws text on the screen.

```typescript
renderer.text(x: number, y: number, r: number, g: number, b: number, a: number, flags: string, max_width: number, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | Top left / center X coordinate | number |
| y | Top left / center Y coordinate | number |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| a | Alpha (opacity) component (0 to 255) | number |
| flags | Text flags: `"+"` for large text, `"-"` for small text, `"c"` for centered text, `"r"` for right-aligned text, `"b"` for bold text, `"d"` for high DPI support. "c" and `"d"` can be combined with the other flags. nil can be specified for normal sized uncentered text. | string |
| max_width | Text will be clipped if it exceeds this width in pixels. Use 0 for no limit. | number |
| text | Text that will be drawn | unknown |
