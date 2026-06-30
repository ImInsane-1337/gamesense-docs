# Simple RGBA Conversion

                                        
This snippet was created and submitted by [kopretinka](https://gamesense.pub/forums/profile.php?id=3494).

                                        
### Description

                                        
Easily convert RGBA to Hex, RGBA to HSVA, and vice-versa.

                                        
## Code

                                        
```lua
local rgba_to_hex = function(r, g, b, a)    return string.format('%02x%02x%02x%02x', r, g, b, a)endlocal hex_to_rgba = function( hex )    hex = hex:gsub('#', '')    return tonumber('0x' .. hex:sub(1, 2)), tonumber('0x' .. hex:sub(3, 4)), tonumber('0x' .. hex:sub(5, 6)), tonumber('0x' .. hex:sub(7, 8)) or 255endlocal hsva_to_rgba = function(h, s, v, a)    local r, g, b    local i = math.floor(h * 6)    local f = h * 6 - i    local p, q, t = v*(1-s), v*(1-f*s), v*(1-(1-f)*s)    i = i % 6    local selection = { { v, t, p }, { q, v, p }, { p, v, t }, { p, q, v }, { t, p, v }, { v, p, q } }    r, g, b = unpack(selection[ i+1 ])    return r * 255, g * 255, b * 255, a * 255endlocal rgba_to_hsva = function(r, g, b, a)    r, g, b, a = r / 255, g / 255, b / 255, a / 255    local max, min = math.max(r, g, b), math.min(r, g, b)    local h, s, v = 0, 0, max    local d = max-min    s = max == 0 and 0 or d/max    if max == min then        h = 0    else        if max == r then        h = (g-b)/ d        if g < b then h = h+6 end        elseif max == g then h = (b-r)/ d+2        elseif max == b then h = (r-g)/ d+4        end          h = h/6    end    return h, s, v, aend
```

                                    
### Minified Version

                                    
```lua
local rgba_to_hex=function(b,c,d,e)return string.format('%02x%02x%02x%02x',b,c,d,e)endlocal hex_to_rgba=function(g)g=g:gsub('#','')return tonumber('0x'..g:sub(1,2)),tonumber('0x'..g:sub(3,4)),tonumber('0x'..g:sub(5,6)),tonumber('0x'..g:sub(7,8))or 255 endlocal hsva_to_rgba=function(i,j,k,e)local b,c,d;local l=math.floor(i*6)local m=i*6-l;local n,o,p=k*(1-j),k*(1-m*j),k*(1-(1-m)*j)l=l%6;local q={{k,p,n},{o,k,n},{n,k,p},{n,o,k},{p,n,k},{k,n,o}}b,c,d=unpack(q[l+1])return b*255,c*255,d*255,e*255 endlocal rgba_to_hsva=function(b,c,d,e)b,c,d,e=b/255,c/255,d/255,e/255;local s,t=math.max(b,c,d),math.min(b,c,d)local i,j,k=0,0,s;local u=s-t;j=s==0 and 0 or u/s;if s==t then i=0 else if s==b then i=(c-d)/u;if c<d then i=i+6 end elseif s==c then i=(d-b)/u+2 elseif s==d then i=(b-c)/u+4 end;i=i/6 end;return i,j,k,e end
```
