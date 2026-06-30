# renderer.load_rgba

Loads a texture from a RGBA buffer. Returns a texture ID that can be used with renderer.texture, or nil on failure

```typescript
renderer.load_rgba(contents: string, width: number, height: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| contents | RGBA buffer (byte encoded - red = "\xFF\x00\x00\xFF") | string |
| width | Width | number |
| height | Height | number |

Returns `texture: number`
