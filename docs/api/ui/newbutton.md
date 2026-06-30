# ui.new_button

Throws an error on failure. The return value should not be used with ui.set or ui.get.

```typescript
ui.new_button(tab: string, container: string, name: string, callback): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this checkbox will be added. | string |
| name | The name of the button. | string |
| callback | The lua function that will be called when the button is pressed. | function |

Returns `menu item: number`
