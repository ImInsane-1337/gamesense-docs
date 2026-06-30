# General

pui will get more features soon

## How to include pui?

You have to subscribe to the library in the workshop.

```
local pui = require("gamesense/pui")
```



## Perfect strings or pui.format(s)

While gamesense supports multicolored text, *pui* makes the use of it much more convenient.

gamesense UI elements have a limit of a string length. If your script is not loading, shorten your strings or simplify them (remove gradients).
Control characterDescription
| `\v` | Accent color. Can be overridden via setting `pui.accent` |
| `\r` | Reverts the default color of the text. |
| `\f<macro>` | Macros. See examples to learn more. |
| `\bFFFFFF...[text]` | Gradient text. Example: `\bFF0000\b00FF00[Happy new year!]` |
| `\aFFFFFFFF` | Custom color. Works in gamesense ui as well. |

If you want to force perfect string, use `pui.format(text)`, for example: in values of a combobox. You don't need to use if it's already supported.

Study these examples to learn more:

#### Accent color:

```
local group = group

group:label("\vHello world!\r I mean, wassup g?")

pui.accent = "24EE24FF"
group:label("\vUhhh, who changed the color?")
```

#### Gradients:

```
group:label("\bFF0000\b00FF00[Happy new year]!")
group:label("\bFFFFFFFF\bFFFFFF00[Fadeeeeeeeeeee]")
```

**Macros**

```
pui.macros.title = "PUI"

pui.checkbox("LUA", "A", "\f<title> Enable")
pui.combobox("LUA", "A", "\f<title> Items", {"A", "B", "C"})
```
