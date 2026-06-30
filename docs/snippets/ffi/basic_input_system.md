# Basic Input System

                                        
This snippet was created and submitted by [h4x0r1337](https://gamesense.pub/forums/profile.php?id=12351).

                                        
### Description

                                        
A basic way to interact with the game-engine's input system.

                                        
## Code

                                        
```lua
local ffi = require "ffi"local ffi_string, vtable_bind, getmetatable, setmetatable = ffi.string, vtable_bind, getmetatable, setmetatable-- Modulelocal ButtonCode_t = {}local ButtonCode_mt = { __index = ButtonCode_t, __metatable = "ButtonCode_t" }--[[ Sorted by the vtable | https://github.com/perilouswithadollarsign/cstrike15_src/blob/master/public/inputsystem/iinputsystem.h#L89]]local native_IsButtonDown = vtable_bind("inputsystem.dll", "InputSystemVersion001", 15, "bool(__thiscall*)(void*, int)")local native_GetButtonPressedTick = vtable_bind("inputsystem.dll", "InputSystemVersion001", 16, "int(__thiscall*)(void*, int)")local native_GetButtonReleasedTick = vtable_bind("inputsystem.dll", "InputSystemVersion001", 17, "int(__thiscall*)(void*, int)")local native_ButtonCodeToString = vtable_bind("inputsystem.dll", "InputSystemVersion001", 40, "const char*(__thiscall*)(void*, int)")local native_ButtonCodeToVirtualKey = vtable_bind("inputsystem.dll", "InputSystemVersion001", 46, "int(__thiscall*)(void*, int)")function is_valid_key(value)    return getmetatable(value) == "ButtonCode_t"endfunction ButtonCode_mt.__call(button, buttoncode_new)    buttoncode_new = buttoncode_new or button.button    button.button = buttoncode_newendfunction ButtonCode_mt.__eq(button_a, button_b)    local a, b = button_a, button_b    if is_valid_key(button_a) then a = button_a.button end    if is_valid_key(button_b) then b = button_b.button end    return a == bendfunction ButtonCode_t.new(button)    return setmetatable({ button = button or 0 }, ButtonCode_mt)endfunction ButtonCode_t:is_down()    return native_IsButtonDown(self.button)endfunction ButtonCode_t:get_pressed_tick()    return native_GetButtonPressedTick(self.button)endfunction ButtonCode_t:get_released_tick()    return native_GetButtonReleasedTick(self.button)endfunction ButtonCode_t:to_string()    local string = native_ButtonCodeToString(self.button)    if string[0] ~= nil then return ffi_string(string) end    return nilendfunction ButtonCode_t:to_vkey()    return native_ButtonCodeToVirtualKey(self.button)endreturn ButtonCode_t
```
