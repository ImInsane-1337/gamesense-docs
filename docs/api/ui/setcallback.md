# ui.set_callback

Sets the change callback of a custom menu item. It will be executed on change and passed the reference

```typescript
ui.set_callback(item: number, callback)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| item | The special value returned by ui.new_*. Do not try passing a reference to an existing menu item. | number |
| callback | Lua function that will be called when the menu item changes values. For example, this will be called when the user checks or unchecks a checkbox. | function |
