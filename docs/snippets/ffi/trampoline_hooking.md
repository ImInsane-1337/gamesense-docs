# Trampoline Hooking Library

                                        
This snippet was created and submitted by [h4x0r1337](https://gamesense.pub/forums/profile.php?id=12351) and [chinaman](https://gamesense.pub/forums/profile.php?id=9397).

                                        
### Description

                                        
Allows you to hook functions using the Game Overlay Renderer.

                                        
## Code

                                        
                                            danger
                                            
                                                
This method of hooking is able to be detected!

                                        
                                    
                                    
```lua
local ffi = require "ffi"local Hooking_t = {}local Hooking_mt = { __index = Hooking_t, __metatable = "Hooking_t" }local signature_HookFunc = client.find_signature("GameOverlayRenderer.dll", "\x55\x8B\xEC\x64\xA1\xCC\xCC\xCC\xCC\x6A\xFF\x68\xCC\xCC\xCC\xCC\x50\x64\x89\x25\xCC\xCC\xCC\xCC\x81\xEC\xCC\xCC\xCC\xCC\x53\x8B\x5D") or error "GameOverlayRenderer.dll!::HookFunc could not be found. Signature is outdated."local signature_UnhookFunc = client.find_signature("GameOverlayRenderer.dll", "\x55\x8B\xEC\x64\xA1\xCC\xCC\xCC\xCC\x6A\xFF\x68\xCC\xCC\xCC\xCC\x50\x64\x89\x25\xCC\xCC\xCC\xCC\x81\xEC\xCC\xCC\xCC\xCC\x56\x8B\x75") or error "GameOverlayRenderer.dll!::UnhookFunc could not be found. Signature is outdated."local native_HookFunc = ffi.cast("void(__cdecl*)(void*, void*, uintptr_t*, int*, int)", signature_HookFunc)local native_UnhookFunc = ffi.cast("void(__cdecl*)(void*, bool)", signature_UnhookFunc)local pTrampoline = ffi.new("uintptr_t[1]")local pbSuccess = ffi.new("int[1]")function is_valid_func(value)    return getmetatable(value) == "Hooking_t"endfunction Hooking_mt.__call(hook, ...)    return hook.trampoline(...)endfunction Hooking_t.new(typestring, real_address, new_function)    local real_function = ffi.cast(typestring, real_address)    local hook_function = ffi.cast(typestring, new_function)    if native_HookFunc(real_function, hook_function, pTrampoline, pbSuccess, 0) ~= 0 then        return setmetatable( { real_function = real_function, hook_function = hook_function, trampoline = ffi.cast(typestring, pTrampoline[0]), success = pbSuccess[0] }, Hooking_mt )    endendfunction Hooking_t:unhook()    native_UnhookFunc(self.real_function, false)endreturn Hooking_t
```

                            
## Example

                            
```lua
local hook = require "Hook"local baseclient = client.create_interface("client.dll", "VClient018")local base_vftable = ffi.cast("void***", baseclient)[0]local event = hook.new("void(__stdcall*)(int)", base_vftable[37], function(stage)    print("test")end)client.delay_call(1.0, function()    event:unhook()end)
```
