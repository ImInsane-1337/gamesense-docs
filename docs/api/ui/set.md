# ui.set

For checkboxes, pass true or false. For a slider, pass a number that is within the slider's minimum/maximum values. For a combobox, pass a string value. For a multiselect combobox, pass zero or more strings. For referenced buttons, value is ignored and the button's callback is invoked. For color pickers, pass the arguments r, g, b, a.

```typescript
ui.set(item: number, value: any, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| item | The result of either ui.new_* or ui.reference | number |
| value | The value to which the menu item will be set | any |
| ... | For multiselect comboboxes, you may want to set more than one option. | unknown |
