# renderer.measure_text

Returns width, height. This can only be called from the paint callback.

```typescript
renderer.measure_text(flags: string, ...): number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| flags | Text flags: `"+"` for large text, `"-"` for small text, `"b"` for bold text, `"d"` for high DPI support. "c" and `"d"` can be combined with the other flags. nil can be specified for normal sized text. | string |
| text | Text that will be measured | unknown |

Returns `width: number, height: number`
