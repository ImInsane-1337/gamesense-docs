# writefile
info
Usually the [database API](../database.md) is a better choice for persistent storage.

# writefile

Overwrites the file with the passed text. The file is created if it doesn't exist.

```typescript
writefile(filename: string, text: string)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| filename | The filename relative to the CS:GO directory. | string |
| text | The text to write to the file. | string |
