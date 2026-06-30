# GetPlayerInfo

                                        
This snippet was created by [halflifefan](https://gamesense.pub/forums/profile.php?id=2618) and submitted by [h4x0r1337](https://gamesense.pub/forums/profile.php?id=12351).

                                        
### Description

                                        
Allows you access and read the `PlayerInfo_t` struct effortlessly.

                                        
## Code

                                        
```lua
local ffi = require "ffi"--[[ https://github.com/perilouswithadollarsign/cstrike15_src/blob/master/public/cdll_int.h#L159 ]]local PlayerInfo_t = ffi.typeof([[    struct {        uint64_t version;        uint64_t __xuid;        char __name[128];        int userid;        char __guid[33];        unsigned int friendsID;        char __friendsName[128];        bool __fakeplayer;        bool __ishltv;        unsigned int __custom_files[4];        unsigned char files_downloaded;    }]])local PlayerInfo_t_mt = {}local native_GetPlayerInfo = vtable_bind("engine.dll", "VEngineClient014", 8, "bool(__thiscall*)(void*, int, $*)", PlayerInfo_t)local fallback = {    xuid = function(self) return string.match(tostring(self.__xuid), "%d+") end,    name = function(self) return ffi_.string(self.__name, 128) end,    guid = function(self) return ffi.string(self.__guid, 33) end,    friends_name = function(self) return ffi.string(self.__friendsName, 128) end,    is_fake_client = function(self) return self.__fakeplayer end,    is_hltv = function(self) return self.__ishltv end,    custom_files = function(self)        local custom_files = self.__custom_files        return { custom_files[0], custom_files[1], custom_files[2], custom_files[4] }    end}function PlayerInfo_t_mt:__index(index)    local fallback_fn = fallback[index]    if not fallback_fn then return nil end    return fallback[index](self)endffi.metatype(PlayerInfo_t, PlayerInfo_t_mt)function get_player_info(entindex)    if type(entindex) ~= "number" then return nil end    local out = PlayerInfo_t(0xFFFFFFFFFFFFF002ULL)    if native_GetPlayerInfo(entindex, out) == true then return out end    return nilend
```
