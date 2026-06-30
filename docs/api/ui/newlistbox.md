# ui.new_listbox

Throws an error on failure. Returns a special value that can be used with ui.get. Calling ui.get on a listbox will return the zero-based index of the currently selected string.

```typescript
ui.new_listbox(tab: string, container: string, name: string, items: table): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA | string |
| container | The name of the existing container to which this listbox will be added | string |
| name | Name | string |
| items | Table of items (strings) | table |

Returns `menu item: number`
