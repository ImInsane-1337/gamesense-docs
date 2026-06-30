# client.register_esp_flag
info
Refer to [client.register_esp_flag example](https://gamesense-docs.pages.dev/examples/register_esp_flag) for how to use this function.

# client.register_esp_flag

Requires "Flags" in Player ESP to be enabled.

```typescript
client.register_esp_flag(flag: string, r: number, g: number, b: number, callback)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| flag | String of text that will be shown when callback returns true | string |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| callback | Function that will be called for each entity when esp is drawn. If you return true here, the flag will be shown. You can optionally return a 2nd value to override the text that is drawn. | function |
