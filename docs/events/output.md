# output

## Description

This event lets you override the text drawn in the top left. There can only be one callback for this event. This event callback is invoked from print, client.log, client.color_log, "Missed due to spread" message, etc.

## Arguments

| Index | Name | Type |
| --- | --- | --- |
| 0 | Argument #0 | table |

### #0 - Properties

| Name | Description |
| --- | --- |
| text | Drawn text |
| r | Drawn color: Red 0-255 |
| g | Drawn color: Green 0-255 |
| b | Drawn color: Blue 0-255 |
| a | Alpha 0-255 |
