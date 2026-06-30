# ui.new_label

Creates a new label, this can be used to make otherwise attached menu items standalone or have interactive menus. Returns a special value that can be passed to ui.set, or throws an error on failure.

```typescript
ui.new_label(tab: string, container: string, name: string): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, CONFIG or LUA. | string |
| container | The name of the existing container to which this control will be added. | string |
| name | The name of the label. This can later be changed using ui.set. | string |

Returns `menu item: number`
