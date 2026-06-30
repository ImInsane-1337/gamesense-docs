# renderer.indicator

Draws an indicator on the screen and returns the Y screen coordinate (vertical offset) of the drawn text, or nil on failure.

```typescript
renderer.indicator(r: number, g: number, b: number, a: number, ...): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| a | Alpha (opacity) component (0 to 255) | number |
| text | The text that will be drawn. Additional arguments will be concatenated. | unknown |

Returns `y: number`
