# client.get_cvar
info
In most cases using the [cvar API](../cvar.md) is preferred over this function.

# client.get_cvar

Returns the value of a console variable.

```typescript
client.get_cvar(cvar_name: string): string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| cvar_name | Name of the convar. | string |

Returns `value: string`
