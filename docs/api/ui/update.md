# ui.update

Creates a string UI element, can be used to store arbitrary strings in configs. No menu item is created but it has the same semantics as other ui.new_* functions. Returns a special value that can be passed to ui.get and ui.set, or throws an error on failure.

```typescript
ui.update(item: number, value: any, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| item | The special value returned by ui.new_checkbox, ui.new_slider, ui.new_combobox, ui.new_hotkey, or ui.reference. | number |
| value | The value to which the menu item will be set | any |
| ... | For multiselect comboboxes, you may want to set more than one option. | unknown |
