# renderer.load_svg

Loads a [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG) from a string. The file can for example be loaded using [readfile](../g/readfile.md). Returns a texture ID that can be used with [renderer.texture](loadsvg.md), or nil on failure

```typescript
renderer.load_svg(contents: string, width: number, height: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| contents | SVG file contents | string |
| width | Width | number |
| height | Height | number |

Returns `texture: number`
