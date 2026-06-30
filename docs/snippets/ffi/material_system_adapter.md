# Material System Adapter

                                        
This snippet was created and submitted by [h4x0r1337](https://gamesense.pub/forums/profile.php?id=12351).

                                        
### Description

                                        
Allows you access and read the `RenderAdapterInfo_t` struct effortlessly.

                                        
## Code

                                        
```lua
local ffi = require "ffi"local RenderAdapterInfo_t = ffi.typeof([[    struct {        char __m_pDriverName[512];        unsigned int __m_VendorID;        unsigned int __m_DeviceID;        unsigned int __m_SubSysID;        unsigned int __m_Revision;        int __m_nDXSupportLevel;        int __m_nMinDXSupportLevel;        int __m_nMaxDXSupportLevel;        unsigned int __m_nDriverVersionHigh;        unsigned int __m_nDriverVersionLow;        int64_t pad_0;    }]])local RenderAdapterInfo_mt = { __index = {} }local native_GetCurrentAdapter = vtable_bind("materialsystem.dll", "VMaterialSystem080", 25, "int(__thiscall*)(void*)")local native_GetAdapterInfo = vtable_bind("materialsystem.dll", "VMaterialSystem080", 26, "void(__thiscall*)(void*, int, $*)", RenderAdapterInfo_t)function get_current_adapter()    return native_GetCurrentAdapter()endlocal fallback = {    drivername = function(self) return ffi.string(self.__m_pDriverName) end,    vendorid = function(self) return string.match(tostring(self.__m_VendorID), "%d+") end,    deviceid = function(self) return string.match(tostring(self.__m_DeviceID), "%d+") end,    subsysid = function(self) return string.match(tostring(self.__m_SubSysID), "%d+") end,    revision = function(self) return string.match(tostring(self.__m_Revision), "%d+") end}function RenderAdapterInfo_mt:__index(index)    local fallback_fn = fallback[index]    if not fallback_fn then return nil end    return fallback[index](self)endffi.metatype(RenderAdapterInfo_t, RenderAdapterInfo_mt)function get_adapter_info(adapter)    local info = RenderAdapterInfo_t()    native_GetAdapterInfo(adapter, info)    return infoend
```
