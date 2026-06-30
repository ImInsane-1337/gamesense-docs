# run_command

## Description

Fired every time the game runs a command (usually 64 times a second, equal to tickrate) while you're alive. This is the best event for processing data that only changes when the game receives an update from the server, like information about other players.

## Arguments

| Index | Name | Type |
| --- | --- | --- |
| 0 | Argument #0 | table |

### #0 - Properties

| Name | Description |
| --- | --- |
| chokedcommands | Amount of commands that the client has choked |
| command_number | Current command number |
