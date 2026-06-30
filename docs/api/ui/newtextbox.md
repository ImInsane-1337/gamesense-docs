# ui.new_textbox

Throws an error on failure. Returns a special value that can be used with ui.get

```typescript
ui.new_textbox(tab: string, container: string, name: string): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this textbox will be added. | string |
| name | The name of the textbox | string |

Returns `menu item: number`
