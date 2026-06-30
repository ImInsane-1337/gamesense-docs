# client.fire_event

Fires a custom event that other scripts can listen to using [client.set_event_callback](https://gamesense-docs.pages.dev/api/docs/client/set_event_callback).

```typescript
client.fire_event(event_name: string, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| event_name | Name of the custom event. | string |
| args | Arguments that will be passed to the event callbacks. | unknown |
