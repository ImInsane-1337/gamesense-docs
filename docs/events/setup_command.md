# setup_command

## Description

Fired every time the game prepares a move command that's sent to the server. This is ran before cheat features like antiaim and can be used to modify user input (view angles, pressed keys, movement) how it's seen by the cheat. For example, setting `in_use = 1` will disable antiaim the same way pressing use key ingame does. This is the preferred method of setting user input and should be used instead of `client.exec` whenever possible.

## Arguments

| Index | Name | Type |
| --- | --- | --- |
| 0 | Argument #0 | table |

### #0 - Properties

| Name | Description |
| --- | --- |
| chokedcommands | Amount of commands that the client has choked |
| command_number | Current command number |
| discharge_pending | Set to true to discharge double tap. Does not work with other exploit features |
| pitch | Pitch view angle |
| yaw | Yaw view angle |
| forwardmove | Forward / backward speed (-450 to 450) |
| sidemove | Left / right speed (-450 to 450) |
| move_yaw | Yaw angle that's used for movement. If not set, view yaw is used |
| allow_send_packet | Set to false to make the cheat choke the current command (when possible) |
| no_choke | Set to true to avoid unnecessary choking like fake lag. Some features (like anti-aimbot) don't respect this field |
| quick_stop | Whether or not quick stop is being triggered |
| force_defensive | Set to true to forcibly activate defensive |
| in_attack | IN_ATTACK Button |
| in_jump | IN_JUMP Button |
| in_duck | IN_DUCK Button |
| in_forward | IN_FORWARD Button |
| in_back | IN_BACK Button |
| in_use | IN_USE Button |
| in_cancel | IN_CANCEL Button |
| in_left | IN_LEFT Button |
| in_right | IN_RIGHT Button |
| in_moveleft | IN_MOVELEFT Button |
| in_moveright | IN_MOVERIGHT Button |
| in_attack2 | IN_ATTACK2 Button |
| in_run | IN_RUN Button |
| in_reload | IN_RELOAD Button |
| in_alt1 | IN_ALT1 Button |
| in_alt2 | IN_ALT2 Button |
| in_score | IN_SCORE Button |
| in_speed | IN_SPEED Button |
| in_walk | IN_WALK Button |
| in_zoom | IN_ZOOM Button |
| in_weapon1 | IN_WEAPON1 Button |
| in_weapon2 | IN_WEAPON2 Button |
| in_bullrush | IN_BULLRUSH Button |
| in_grenade1 | IN_GRENADE1 Button |
| in_grenade2 | IN_GRENADE2 Button |
| in_attack3 | IN_ATTACK3 Button |
| weaponselect |  |
| weaponsubtype |  |
