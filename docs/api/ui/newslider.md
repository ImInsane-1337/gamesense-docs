# ui.new_slider

Returns a special value that can be passed to ui.get and ui.set, or throws an error on failure.

```typescript
ui.new_slider(tab: string, container: string, name: string, min: number, max: number, init_value: number, show_tooltip: boolean, unit: string, scale: number, tooltips: table): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this control will be added. | string |
| name | The name of the slider. | string |
| min | The minimum value that can be set using the slider. | number |
| max | The maximum value that can be set using the slider. | number |
| init_value | Integer. The initial value. If not provided, the initial value will be min. | number |
| show_tooltip | Boolean. true if the slider should display its current value. | boolean |
| unit | String that is two characters or less. This will be appended to the display value. For example, "px" for pixels or "%" for a percentage. | string |
| scale | The display value will be multiplied by this scale. For example, 0.1 will make a slider with the range [0-1800] show as 0.0-180.0 with one decimal place. | number |
| tooltips | Table used to override the tooltip for the specified values. The key must be within min-max. The value is a string that will be shown instead of the numeric value whenever that value is selected. | table |

Returns `menu item: number`
