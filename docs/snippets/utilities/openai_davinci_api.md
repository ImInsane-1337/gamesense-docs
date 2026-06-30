# OpenAI Davinci API

                                        
This snippet was created and submitted by [kay](https://gamesense.pub/forums/profile.php?id=1426).

                                        
### Description

                                        
A function to interact with the OpenAI Davinci API and extract a response from it.

                                        
## Code

                                        
```lua
local http = require "gamesense/http"local OPENAI_URL = "https://api.openai.com/v1/engines/davinci/completions"local OPENAI_API_KEY = "API_KEY"local header = {["Content-Type"] = "application/json", ["Authorization"]= "Bearer ".. OPENAI_API_KEY}local function make_ai_memes(text_to_respond_to)    local data ={        ["prompt"]="Person:" .. text_to_respond_to .. "\nFriend:",        ["temperature"]=0.75,        ["max_tokens"]=100,        ["top_p"]=1,        ["stop"]="\n"    }    http.post(OPENAI_URL, {headers = header, body = json.stringify(data)}, function(success, response)        local bot_response = json.parse(response.body).choices[1].text        print(bot_response)        return bot_response    end)endmake_ai_memes("im a god gamer bro, youre dumb as fuck")
```
