# renderer.load_png

Loads a texture from raw PNG contents (with file header). The file can for example be loaded using [readfile](../g/readfile.md). Returns a texture ID that can be used with renderer.texture, or nil on failure

```typescript
renderer.load_png(contents: string, width: number, height: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| contents | PNG file contents | string |
| width | Width | number |
| height | Height | number |

Returns `texture: number`
