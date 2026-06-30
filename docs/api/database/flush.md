# database.flush
danger
This function is slow and performs disk IO. Do not call it too often.

# database.flush

Flushes the database to disk. This is automatically called when the script is reloaded, but you can call it manually if you want to force a flush.

```typescript
database.flush()
```
