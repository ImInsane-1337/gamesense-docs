# ui.new_color_picker

Throws an error on failure. The color picker is placed to the right of the previous menu item.

```typescript
ui.new_color_picker(tab: string, container: string, name: string, r: number, g: number, b: number, a: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this checkbox will be added. | string |
| name | The name of the color picker. This will not be shown, it is only used to identify this item in saved configs. | string |
| r | Initial red value (0-255) | number |
| g | Initial green value (0-255) | number |
| b | Initial blue value (0-255) | number |
| a | Initial alpha value (0-255) | number |

Returns `menu item: number`
