# 2D rounded rectangle with an outline

                                        
This snippet was created and submitted by [LosAngeles](https://gamesense.pub/forums/profile.php?id=8883).

                                        
### Description

                                        
Draws a rounded rectangle with an outline in 2D space.

                                        
## Code

                                        
```lua
function renderer.outlined_rounded_rectangle(x, y, w, h, r, g, b, a, radius, thickness)    y = y + radius    local data_circle = {        {x + radius, y, 180},        {x + w - radius, y, 270},        {x + radius, y + h - radius * 2, 90},        {x + w - radius, y + h - radius * 2, 0},    }    local data = {        {x + radius, y - radius, w - radius * 2, thickness},        {x + radius, y + h - radius - thickness, w - radius * 2, thickness},        {x, y, thickness, h - radius * 2},        {x + w - thickness, y, thickness, h - radius * 2},    }    for _, data in next, data_circle do        renderer.circle_outline(data[1], data[2], r, g, b, a, radius, data[3], 0.25, thickness)    end    for _, data in next, data do        renderer.rectangle(data[1], data[2], data[3], data[4], r, g, b, a)    endend
```
