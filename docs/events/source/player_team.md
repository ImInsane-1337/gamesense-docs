# player_team

## Description

A player changed their team

## Arguments

| Type | Name | Description |
| --- | --- | --- |
| short | userid | user ID on the server |
| byte | team | team id |
| byte | oldteam | old team id |
| bool | disconnect | team change because player disconnects |
| bool | autoteam | true if the player was auto assigned to the team (OB only) |
| bool | silent | if true wont print the team join messages (OB only) |
| string | name | player's name (OB only) |
