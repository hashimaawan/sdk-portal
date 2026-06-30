# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/ruby/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ruby
def shotchartdetail_get(season_type,
                        team_id,
                        player_id,
                        game_id,
                        outcome,
                        location,
                        month,
                        season_segment,
                        date_from,
                        date_to,
                        opponent_team_id,
                        vs_conference,
                        vs_division,
                        position,
                        rookie_year,
                        game_segment,
                        period,
                        last_n_games,
                        context_measure)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season_type` | `String` | Query, Required | - |
| `team_id` | `String` | Query, Required | - |
| `player_id` | `String` | Query, Required | - |
| `game_id` | `String` | Query, Required | - |
| `outcome` | `String` | Query, Required | - |
| `location` | `String` | Query, Required | - |
| `month` | `String` | Query, Required | - |
| `season_segment` | `String` | Query, Required | - |
| `date_from` | `String` | Query, Required | - |
| `date_to` | `String` | Query, Required | - |
| `opponent_team_id` | `String` | Query, Required | - |
| `vs_conference` | `String` | Query, Required | - |
| `vs_division` | `String` | Query, Required | - |
| `position` | `String` | Query, Required | - |
| `rookie_year` | `String` | Query, Required | - |
| `game_segment` | `String` | Query, Required | - |
| `period` | `String` | Query, Required | - |
| `last_n_games` | `String` | Query, Required | - |
| `context_measure` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
season_type = 'SeasonType8'

team_id = 'TeamID8'

player_id = 'PlayerID6'

game_id = 'GameID8'

outcome = 'Outcome4'

location = 'Location4'

month = 'Month0'

season_segment = 'SeasonSegment8'

date_from = 'DateFrom6'

date_to = 'DateTo0'

opponent_team_id = 'OpponentTeamID6'

vs_conference = 'VsConference6'

vs_division = 'VsDivision6'

position = 'Position8'

rookie_year = 'RookieYear8'

game_segment = 'GameSegment6'

period = 'Period2'

last_n_games = 'LastNGames4'

context_measure = 'ContextMeasure2'

client_controller.shotchartdetail_get(
  season_type,
  team_id,
  player_id,
  game_id,
  outcome,
  location,
  month,
  season_segment,
  date_from,
  date_to,
  opponent_team_id,
  vs_conference,
  vs_division,
  position,
  rookie_year,
  game_segment,
  period,
  last_n_games,
  context_measure
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



