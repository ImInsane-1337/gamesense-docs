# ui.new_hotkey

Returns a special value that can be passed to ui.get to see if the hotkey is pressed, or throws an error on failure.

```typescript
ui.new_hotkey(tab: string, container: string, name: string, inline: boolean, default_hotkey: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| tab | The name of the tab: RAGE, AA, LEGIT, VISUALS, MISC, SKINS, PLAYERS, LUA. | string |
| container | The name of the existing container to which this control will be added. | string |
| name | The name of the hotkey. | string |
| inline | Boolean. If set to true, the hotkey will be placed to the right of the preceding menu item. | boolean |
| default_hotkey | Virtual key | number |

Returns `menu item: number`
