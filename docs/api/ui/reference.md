# ui.reference

Avoid calling this from inside a function. Returns a reference that can be passed to ui.get and ui.set, or throws an error on failure. This allows you to access a built-in pre-existing menu items. This function returns multiple values when the specified menu item is followed by unnamed menu items, for example a color picker or a hotkey.

```typescript
ui.reference(tab: string, container: string, name: string): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this checkbox will be added. | string |
| name | The name of the menu item. | string |

Returns `menu item: number`
