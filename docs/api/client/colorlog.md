# client.color_log

Logs a colored message to console. End the string with \0 to prevent it from adding a newline.

```typescript
client.color_log(r: number, g: number, b: number, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| msg | The message to be logged. Pass additional arguments to concatenate them to the message. | string |
