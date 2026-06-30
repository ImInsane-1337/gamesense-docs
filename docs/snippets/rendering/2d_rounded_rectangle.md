# 2D rounded rectangle

                                        
This snippet was created and submitted by [LosAngeles](https://gamesense.pub/forums/profile.php?id=8883).

                                        
### Description

                                        
Draws a rounded rectangle in 2D space.

                                        
## Code

                                        
```lua
renderer.rounded_rectangle = function(x, y, w, h, r, g, b, a, radius)    y = y + radius    local data_circle = {        {x + radius, y, 180},        {x + w - radius, y, 90},        {x + radius, y + h - radius * 2, 270},        {x + w - radius, y + h - radius * 2, 0},    }    local data = {        {x + radius, y, w - radius * 2, h - radius * 2},        {x + radius, y - radius, w - radius * 2, radius},        {x + radius, y + h - radius * 2, w - radius * 2, radius},        {x, y, radius, h - radius * 2},        {x + w - radius, y, radius, h - radius * 2},    }    for _, data in next, data_circle do        renderer.circle(data[1], data[2], r, g, b, a, radius, data[3], 0.25)    end    for _, data in next, data do        renderer.rectangle(data[1], data[2], data[3], data[4], r, g, b, a)    endend
```
