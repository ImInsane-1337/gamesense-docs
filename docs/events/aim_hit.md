# aim_hit

## Description

Fired when the rage aimbot hit a shot at a player.

## Example

```lua
local hitgroup_names = {"generic", "head", "chest", "stomach", "left arm", "right arm", "left leg", "right leg", "neck", "?", "gear"}local function aim_hit(e)    local group = hitgroup_names[e.hitgroup + 1] or "?"    print(string.format(        "Hit %s in the %s for %d damage (%d health remaining)",        entity.get_player_name(e.target), group, e.damage,        entity.get_prop(e.target, "m_iHealth")    ))endclient.set_event_callback("aim_hit", aim_hit)
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
| hitgroup | Hit group that was hit. This is not the same thing as a hitbox |
| damage | Actual damage the shot did |
