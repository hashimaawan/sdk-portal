# Homepagev 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdldjJfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def homepagev2_get(stat_type,
                   league_id,
                   season,
                   season_type,
                   player_or_team,
                   player_scope,
                   game_scope,
                   game: nil,
                   player: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stat_type` | `String` | Query, Required | - |
| `league_id` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
| `player_or_team` | `String` | Query, Required | - |
| `player_scope` | `String` | Query, Required | - |
| `game_scope` | `String` | Query, Required | - |
| `game` | `String` | Query, Optional | - |
| `player` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
stat_type = 'StatType8'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

player_or_team = 'PlayerOrTeam8'

player_scope = 'PlayerScope2'

game_scope = 'GameScope0'

client_controller.homepagev2_get(
  stat_type,
  league_id,
  season,
  season_type,
  player_or_team,
  player_scope,
  game_scope
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



