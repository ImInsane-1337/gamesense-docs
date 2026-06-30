# renderer.load_jpg

Loads a texture from raw JPG contents (with file header). The file can for example be loaded using [readfile](../g/readfile.md). Returns a texture ID that can be used with renderer.texture, or nil on failure

```typescript
renderer.load_jpg(contents: string, width: number, height: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| contents | JPG file contents | string |
| width | Width | number |
| height | Height | number |

Returns `texture: number`
