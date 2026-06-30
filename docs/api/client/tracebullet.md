# client.trace_bullet

Returns entindex, damage. Entindex is nil when no player is hit or if players are skipped.

```typescript
client.trace_bullet(from_player: number, from_x: number, from_y: number, from_z: number, to_x: number, to_y: number, to_z: number, skip_players: boolean): number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| from_player | Entity index of the player whose weapon will be used for this trace | number |
| from_x | X coordinate of the start of the trace | number |
| from_y | Y coordinate of the start of the trace | number |
| from_z | Z coordinate of the start of the trace | number |
| to_x | X coordinate of the end of the trace | number |
| to_y | Y coordinate of the end of the trace | number |
| to_z | Z coordinate of the end of the trace | number |
| skip_players | Pass true to skip expensive hitbox checks. | boolean |

Returns `entindex: number, damage: number`
