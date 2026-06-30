# round_end

## Arguments

| Type | Name | Description |
| --- | --- | --- |
| byte | winner | winner team/user id |
| byte | reason | reason why team won |
| string | message | end round message |
| byte | legacy | server-generated legacy value |
| short | player_count | total number of players alive at the end of round, used for statistics gathering, computed on the server in the event client is in replay when receiving this message |
| byte | nomusic | if set, don't play round end music, because action is still on-going |
