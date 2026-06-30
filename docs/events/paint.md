# paint

## Description

Fired every time the game renders a frame while being connected to a server. Can be used to draw to the screen using the [renderer.*](https://gamesense-docs.pages.dev/docs/developers/globals/renderer) functions.

## Example

```lua
client.set_event_callback("paint", function()    renderer.text(15, 15, 255, 255, 255, 255, nil, 0, "hello world")end)
```
