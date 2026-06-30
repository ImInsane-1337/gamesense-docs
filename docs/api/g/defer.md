# defer

Registers a function to be called at lua shutdown/reload, equivalent to `client.set_event_callback("shutdown", callback)`.

```typescript
defer(callback)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| callback | The function to execute on shutdown. | function |
