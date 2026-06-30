# ui.get

For a checkbox, returns true or false. For a slider, returns an integer. For a combobox, returns a string. For a multiselect combobox, returns an array of strings. For a hotkey, returns true if the hotkey is active. For a color picker, returns r, g, b, a. Throws an error on failure.

```typescript
ui.get(item: number): any
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| item | The special value returned by ui.new_checkbox, ui.new_slider, ui.new_combobox, ui.new_hotkey, or ui.reference. | number |

Returns `the current value of the menu item: any`
