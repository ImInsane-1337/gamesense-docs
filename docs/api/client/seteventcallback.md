# client.set_event_callback

Registers the function as a callback for the specified event.
It can be removed later using [client.unset_event_callback](seteventcallback.md).

```typescript
client.set_event_callback(event_name: string, callback)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| event_name | Name of the event. | string |
| callback | Lua function to call when this event occurs. | function |
