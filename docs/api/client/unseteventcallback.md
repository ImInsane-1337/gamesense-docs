# client.unset_event_callback

Removes a callback that was previously set using [client.set_event_callback](unseteventcallback.md).

```typescript
client.unset_event_callback(event_name: string, callback)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| event_name | Name of the event | string |
| callback | Lua function that was passed to set_event_callback | function |
