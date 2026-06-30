# renderer.texture

Draws a texture from the texture id created from [load_rgba](texture.md), [load_png](texture.md), [load_jpg](texture.md) or [load_svg](texture.md)

```typescript
renderer.texture(texture: number, x: number, y: number, w: number, h: number, r: number, g: number, b: number, a: number, mode: string)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| texture | Texture ID | number |
| x | X screen coordinate | number |
| y | Y screen coordinate | number |
| w | Width | number |
| h | Height | number |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| a | Alpha (opacity) component (0 to 255) | number |
| mode | `"f"` for filled, `"r"` for repeat, otherwise automatic | string |
