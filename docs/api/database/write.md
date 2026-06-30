# database.write
info
Make sure to use unique names for your DB keys to avoid conflicts with other scripts. For example, prefer `"gamesense_watermark_position"` over something generic like `"position"`

# database.write

Writes a value to the database. Avoid calling this often. For example, call read at script load, then call write during the 'shutdown' event

```typescript
database.write(key_name: string, value)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| key_name | String used as a name of the key. | string |
| value | Value the key should be set to. This can be anything that can be sanitized (no functions, userdata). Tables are allowed and encouraged to reduce the amount of database keys your script needs. | unknown |
