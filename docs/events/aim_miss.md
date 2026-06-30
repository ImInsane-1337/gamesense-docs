# aim_miss

## Description

Fired when the rage aimbot missed a shot at a player.

## Example

```lua
local hitgroup_names = {"generic", "head", "chest", "stomach", "left arm", "right arm", "left leg", "right leg", "neck", "?", "gear"}local function aim_miss(e)    local group = hitgroup_names[e.hitgroup + 1] or "?"    print(string.format(        "Missed %s (%s) due to %s",        entity.get_player_name(e.target), group, e.reason    ))endclient.set_event_callback("aim_miss", aim_miss)
```

## Arguments

| Index | Name | Type |
| --- | --- | --- |
| 0 | Argument #0 | table |

### #0 - Properties

| Name | Description |
| --- | --- |
| id | Shot ID, the corresponding aim_fire event has the same ID |
| target | Target player entindex |
| hit_chance | Actual hit chance the shot had |
| hitgroup | Hit group that was missed. This is not the same thing as a hitbox |
| reason | Reason the shot was missed. This can be 'spread', 'prediction error', 'death' or '?' (unknown / resolver) |
