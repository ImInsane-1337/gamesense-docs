# Methods

Learn more about methods of a pui element
Complete list of methods[](#complete-list-of-methods)
- `set(...)`
- `get(find)`
- `override(value)`
- `get_original()`
- `reset()`
- `update(list)`
- `get_list()`
- `get_color()`
- `set_color(...)`
- `get_hotkey()`
- `set_hotkey()`
- `is_reference()`
- `get_type()`
- `get_name()`
- `set_visible(state)`
- `set_enabled(state)`
- `depend(pair1, pair2, ..., pairn)`
- `set_callback(fn, once)`
- `detach_callback(fn)`
- `invoke(...)`

Metamethods:

- `__type = "pui::element" / "pui::group" / "pui::player_slot"`
- `__name = "pui::element" / "pui::group"`
- `__tostring -- e.g. pui.checkbox[18] "Enable" `
- `__call() = get()`
- `__call(...) = set(...)`
- `__metatable = false`

## :override(...)

:override is a feature in gamesense pui version that allows you to override values of elements and easily revert them like in neverlose.

```
local enable_aa = pui.reference("AA", "Anti-aimbot angles", "Enabled")

-- disabling aa:
enable_aa:override(false)

-- don't leave a mess behind you
defer(function()
    enable:override() -- or enable:override(nil)
end)
```

if you need the original value while the element is overridden, use `:get_original()`



## :depend(...)

Sometimes you want to hide certain elements to not mess up the menu. It might look simple but actually it's rather difficult and complicated. But *pui* can make this as easy as pie.

`:depend(...)` is a method of a pui element, which creates a dependence on elements passed as arguments.

Its arguments can be either elements themselves (generally switches), or tables, which contain `ref, condition, ...`.

In most of the cases, it looks like this: `:depend( {ref, condition}, {ref2, condition2}, ... )`

You can also invert conditions like this: `{ref, condition, true}`

If you want to lock elements instead of hiding them: `:depend(true, ...)`

#### Study these examples:

This is a common example of the use of `:depend(...)`. As you can see, there are two labels showing statuses of a switch.

If you want to show your elements when a certain value is selected in a combobox, this can be done as well.

You can add multiple variants for comboboxes

You can define ranges for sliders like this:

Sometimes the condition may be too complicated. In this case, you can use a function:

Yes, you can add more conditions calling `:depend(..)` multiple times. But you don't have to.

Study this example of a password puzzle:

There are a lot of ways to use `:depend()` that I can't even imagine.



## :set_callback(func, once*)

It's pretty much the same as the built-in `ui.set_callback()`, but pui allows you to add multiple callbacks and execute them at least once. You can also unset them by using `:unset_callback(func)` . You can't unset anonymous functions.



## :set_event(event, func, condition*)

This methods is used to call functions in events when a certain condition is met. You can unset this behavior via `:unset_event(event, func)`. You can't unset anonymous functions.



## :get_color() and :get_hotkey()

These will return the value of an additional elements.

Hotkeys states in .value are only updated when activating settings a keybind. Use `:get_hotkey()` to always get the actual key.

##
