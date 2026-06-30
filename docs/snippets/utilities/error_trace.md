# Error Tracing

                                        
This snippet was created and submitted by [LosAngeles](https://gamesense.pub/forums/profile.php?id=8883).

                                        
### Description

                                        
A function to print an error trace, with a default limit of `10`.

                                        
## Code

                                        
```lua
function error_trace(err)    local stack = {err}    local level = 2    while true do        local success, _ = pcall(getfenv, level)        if not success or level >= 10 then            break        end        local _, level_err = pcall(error, "", level)        if level_err ~= "" then            table.insert(stack, level .. ": " .. level_err:sub(1, #level_err - 2))        end        level = level + 1    end    error(table.concat(stack, "\n    "))end
```
