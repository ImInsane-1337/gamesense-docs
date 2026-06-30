# Main

How to create an element? There are a ton of ways, and you'll know all of them

## Defining tab and container

`pui.group(tab, name)` : `pui::group`

```
local checkbox = pui.checkbox("LUA", "A", "Name")
```

```
local group = pui.group("LUA", "A")

group:checkbox("Name")
-- or
pui.checkbox(group, "Name")
```



## Creating an element : pui::element

`pui.element(tab, container, ..., additional, savable)`

`group:element(..., tooltip, savable)`

You can use elements just like in gamesense. All arguments will be saved, and you will also be able to add more *(but there are some exceptions)*
Common example
```
local group = pui.create("Visuals", "Indicators")

-- both are the same:
pui.checkbox(group, "Name", {255, 255, 255}
group:checkbox("Name", {255, 255, 255})
```

#### Exceptions for elements with list (combo, selectable, list, listable)

Due to their arguments style, you will have to modify them a bit in order to use pui features. You can still use them like they are if you don't need to use the additional features.

```
group:combobox("A", "Apple", "Banana", "Coconut")

-- place combo values in a table:
group:combobox("B", {"Apple", "Banana", "Coconut"}, {255})

-- won't work: group:combobox("C", "Apple", "Banana", "Coconut", {255})
```



## What does a pui::element contain?

`pui::element` is a table of variables that you can use in some cases.

For example: `switch.value` return current switch value
VariableDescription
| `.value` | Current value. Includes overridden one too. |
| `.ref` | Original gamesense reference. |
| `.name` | Name of an element. Doesn't include *perfect string* symbols. |
| `.type` | Type of an element. |
VariableDescription
| `.color` | If you passed color as an additional element |
| `.hotkey` | If you passed hotkey as an additional element |



## Arguments and features

Additional elements are hotkeys and color pickers than can be placed near main elements. They are pui elements too.

#### Example

This example shows a switch. It contains children elements: `bar` and `button`. Also you can see, that you may operate them just like regular *pui *elements. These elements will be shown only if the main switch is enabled (`true`).

#### Accesing children elements

Some things should not be saved into configs. You can define which elements should not be saved.

By default, every element is allowed to be saved. Pass `false` to alter that.

#### Example:



## Player list handler

**gamesense **player list is a special tab in the menu that is used to configure settings for each player.  **pui **has got a plist handler that allows you to easily manage your elements and not bothering about updating and saving them.

#### Creating

`pui.plist` is a built-in pui group that supports player list behavior. Creating plist elements is just as easy as regular elements:

#### Getting and setting values

This is a bit more complex. To access a *player slot* (value of an element for a specific player), you should use `ent_index` of this player:

#### Using as regular elements

Though the behavior of these elements is quite different, they are still pui elements. Therefore, you can use methods like `set_callback(), depend(), set_visible(), etc.` but with some exceptions:

`:override()`, `:reset(), :set()` only affect the settings of a selected player.

Override and reset are not supported in player slots yet.
