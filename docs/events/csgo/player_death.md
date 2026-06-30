# player_death

## Description

When a client dies

## Arguments

| Type | Name | Description |
| --- | --- | --- |
| short | userid | user ID who died |
| short | attacker | user ID who killed |
| short | assister | user ID who assisted in the kill |
| bool | assistedflash | assister helped with a flash |
| string | weapon | weapon name killer used |
| string | weapon_itemid | inventory item id of weapon killer used |
| string | weapon_fauxitemid | faux item id of weapon killer used |
| string | weapon_originalowner_xuid |  |
| bool | headshot | signals a headshot |
| short | dominated | did killer dominate victim with this kill |
| short | revenge | did killer get revenge on victim with this kill |
| short | wipe | To do: check if indicates on a squad wipeout in Danger Zone |
| short | penetrated | number of objects shot penetrated before killing target |
| bool | noreplay | if replay data is unavailable, this will be present and set to false |
| bool | noscope | kill happened without a scope, used for death notice icon |
| bool | thrusmoke | hitscan weapon went through smoke grenade |
| bool | attackerblind | attacker was blind from flashbang |
| float | distance | distance to victim in meters |
