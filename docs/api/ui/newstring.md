# ui.new_string

Creates a string UI element, can be used to store arbitrary strings in configs. No menu item is created but it has the same semantics as other ui.new_* functions. Returns a special value that can be passed to ui.get and ui.set, or throws an error on failure.

```typescript
ui.new_string(name: string, default_value: string): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| name | The name of the string element, make sure this is unique. | string |
| default_value | String that specifies the default value. | string |

Returns `menu item: number`
