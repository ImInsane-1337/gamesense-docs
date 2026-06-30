# globals

## Description

Global variables used by the source engine.

## Functions

### absoluteframetime
[globals.absoluteframetime(): number](globals/absoluteframetime.md)
> The absolute time the last frame took to render.

### chokedcommands
[globals.chokedcommands(): number](globals/chokedcommands.md)
> The number of choked commands (commands that haven't yet been sent to the server, for example due to fake lag)

### commandack
[globals.commandack(): number](globals/commandack.md)
> The command number of the most recent server-acknowledged command.

### curtime
[globals.curtime(): number](globals/curtime.md)
> The elapsed game time in seconds. This number is synchronized with the server.

### framecount
[globals.framecount(): number](globals/framecount.md)
> The number of frames rendered since the game started

### frametime
[globals.frametime(): number](globals/frametime.md)
> The time the last frame took to render.

### lastoutgoingcommand
[globals.lastoutgoingcommand(): number](globals/lastoutgoingcommand.md)
> The command number of the most recent sent command.

### mapname
[globals.mapname(): string](globals/mapname.md)
> The name of the loaded map, or nil if you are not in game.

### maxplayers
[globals.maxplayers(): number](globals/maxplayers.md)
> The maximum number of players in a game (usually 64)

### oldcommandack
[globals.oldcommandack(): number](globals/oldcommandack.md)
> The command number of the previous server-acknowledged command.

### realtime
[globals.realtime(): number](globals/realtime.md)
> The time in seconds since the game was started.

### servertickcount
[globals.servertickcount(): number](globals/servertickcount.md)
> Returns the most recently receieved tick from the server.

### tickcount
[globals.tickcount(): number](globals/tickcount.md)
> The number of ticks elapsed on the server.

### tickinterval
[globals.tickinterval(): number](globals/tickinterval.md)
> The time between ticks in seconds, 1/64 for 64 tick.
