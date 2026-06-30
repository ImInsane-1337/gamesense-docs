# entity.get_players

Returns an array of player entity indices. Dormant and dead players will not be added to the list.

```typescript
entity.get_players(enemies_only: boolean): table
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| enemies_only | If true then the local player and teammates will not be added to the list. | boolean |

Returns `table`
