# 3D rectangle with an outline

                                        
This snippet was created and submitted by [gl0ck](https://gamesense.pub/forums/profile.php?id=7770).

                                        
### Description

                                        
Draws a rectangle in 3D space with an outline.

                                        
- `pos` is a vector of world coordinates
- `w` is the width of the rectangle
- `h` is the height of the rectangle
- `r` represents the red value between `0` and `255`
- `g` represents the green value between `0` and `255`
- `b` represents the blue value between `0` and `255`
- `a` represents the alpha value between `0` and `255`

                                        
## Code

                                        
```lua
renderer.rectangle_outline_3d = function(pos, w, h, r, g, b, a)    local old = {}    for rot = 0, 360, 90 do        local rad_rot = math.rad(rot)        local cos_rot = math.cos(rad_rot)        local sin_rot = math.sin(rad_rot)        local line = vector(w * cos_rot + pos.x, h * sin_rot + pos.y, pos.z)        local w2s = { renderer.world_to_screen(line.x, line.y, line.z) }        if w2s[1] and old[1] then            for i = 1, 1 do                local i = i - 1                renderer.line(w2s[1], w2s[2] - i, old[1], old[2] - i, r, g, b, a)            end        end        old = { w2s[1], w2s[2] }    endend
```
