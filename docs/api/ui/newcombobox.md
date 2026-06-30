# ui.new_combobox

Returns a special value that can be passed to ui.get and ui.set, or throws an error on failure.

```typescript
ui.new_combobox(tab: string, container: string, name: string, ...): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this control will be added. | string |
| name | The name of the combobox. | string |
| ... | One or more comma separated string values that will be added to the combobox. Alternatively, a table of strings that will be added. | unknown |

Returns `menu item: number`
