# client.draw_hitboxes

Draws hitbox overlays. Avoid calling this during the paint event.

```typescript
client.draw_hitboxes(entindex: number, duration: number, hitboxes: number, r: number, g: number, b: number, a: number, tick: number)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| entindex | Entity index of the player | number |
| duration | Time in seconds | number |
| hitboxes | Either the [hitbox index](https://gamesense-docs.pages.dev/constants/hitboxes) or 19 for all hitboxes | number |
| r | Red color component (0 to 255) | number |
| g | Green color component (0 to 255) | number |
| b | Blue color component (0 to 255) | number |
| a | Alpha (opacity) component (0 to 255) | number |
| tick | Tick to draw the hitboxes for | number |
