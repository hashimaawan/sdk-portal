# Leaderstiles GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxlYWRlcnN0aWxlc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ruby
def leaderstiles_get(stat,
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
| `stat` | `String` | Query, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
stat = 'Stat2'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

player_or_team = 'PlayerOrTeam8'

player_scope = 'PlayerScope2'

game_scope = 'GameScope0'

result = client_api.leaderstiles_get(
  stat,
  league_id,
  season,
  season_type,
  player_or_team,
  player_scope,
  game_scope
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



