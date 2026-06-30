# console_input

## Description

Fired every time the user types something in the game console and presses enter. Return true from the event handler to make the game not process the input.

## Example

```lua
client.set_event_callback("console_input", function(text)    client.log("entered: '", text, "'")end)
```

## Arguments

| Index | Name | Type |
| --- | --- | --- |
| 0 | console input text | string |
