# aim_fire

## Description

Fired when the rage aimbot shoots at a player.

## Example

```lua
local hitgroup_names = {"generic", "head", "chest", "stomach", "left arm", "right arm", "left leg", "right leg", "neck", "?", "gear"}local function aim_fire(e)    local flags = {        e.teleported and "T" or "",        e.interpolated and "I" or "",        e.extrapolated and "E" or "",        e.boosted and "B" or "",        e.high_priority and "H" or ""    }    local group = hitgroup_names[e.hitgroup + 1] or "?"    print(string.format(        "Fired at %s (%s) for %d dmg (chance=%d%%, bt=%2d, flags=%s)",        entity.get_player_name(e.target), group, e.damage,        math.floor(e.hit_chance + 0.5), globals.toticks(e.backtrack),        table.concat(flags)    ))endclient.set_event_callback("aim_fire", aim_fire)
```

## Arguments

| Index | Name | Type |
| --- | --- | --- |
| 0 | Argument #0 | table |

### #0 - Properties

| Name | Description |
| --- | --- |
| id | Shot ID, this can be used to find the corresponding aim_hit / aim_miss event |
| target | Target player entindex |
| hit_chance | Chance the shot will hit, depends on spread |
| hitgroup | Targeted hit group, this is not the same thing as a hitbox |
| damage | Predicted damage the shot will do |
| backtrack | Amount of ticks the player was backtracked |
| boosted | True if accuracy boost was used to increase the accuracy of the shot |
| high_priority | True if the shot was at a high priority record, like on shot backtrack |
| interpolated | Player was interpolated |
| extrapolated | Player was extrapolated |
| teleported | Target player was teleporting (breaking lag compensation) |
| tick | Tick the shot was fired at. This can be used to draw the hitboxes using client.draw_hitboxes |
| x | X world coordinate of the aim point |
| y | X world coordinate of the aim point |
| z | Z world coordinate of the aim point |
