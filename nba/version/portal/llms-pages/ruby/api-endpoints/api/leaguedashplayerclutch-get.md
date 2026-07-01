# Leaguedashplayerclutch GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJjbHV0Y2hfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def leaguedashplayerclutch_get(clutch_time,
                               ahead_behind,
                               point_diff,
                               game_scope,
                               player_experience,
                               player_position,
                               starter_bench,
                               measure_type,
                               per_mode,
                               plus_minus,
                               pace_adjust,
                               rank,
                               season,
                               season_type,
                               outcome,
                               location,
                               month,
                               season_segment,
                               date_from,
                               date_to,
                               opponent_team_id,
                               vs_conference,
                               vs_division,
                               game_segment,
                               period,
                               last_n_games)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clutch_time` | `String` | Query, Required | - |
| `ahead_behind` | `String` | Query, Required | - |
| `point_diff` | `String` | Query, Required | - |
| `game_scope` | `String` | Query, Required | - |
| `player_experience` | `String` | Query, Required | - |
| `player_position` | `String` | Query, Required | - |
| `starter_bench` | `String` | Query, Required | - |
| `measure_type` | `String` | Query, Required | - |
| `per_mode` | `String` | Query, Required | - |
| `plus_minus` | `String` | Query, Required | - |
| `pace_adjust` | `String` | Query, Required | - |
| `rank` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
| `outcome` | `String` | Query, Required | - |
| `location` | `String` | Query, Required | - |
| `month` | `String` | Query, Required | - |
| `season_segment` | `String` | Query, Required | - |
| `date_from` | `String` | Query, Required | - |
| `date_to` | `String` | Query, Required | - |
| `opponent_team_id` | `String` | Query, Required | - |
| `vs_conference` | `String` | Query, Required | - |
| `vs_division` | `String` | Query, Required | - |
| `game_segment` | `String` | Query, Required | - |
| `period` | `String` | Query, Required | - |
| `last_n_games` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
clutch_time = 'ClutchTime4'

ahead_behind = 'AheadBehind8'

point_diff = 'PointDiff6'

game_scope = 'GameScope0'

player_experience = 'PlayerExperience4'

player_position = 'PlayerPosition8'

starter_bench = 'StarterBench0'

measure_type = 'MeasureType8'

per_mode = 'PerMode6'

plus_minus = 'PlusMinus0'

pace_adjust = 'PaceAdjust2'

rank = 'Rank2'

season = 'Season0'

season_type = 'SeasonType8'

outcome = 'Outcome4'

location = 'Location4'

month = 'Month0'

season_segment = 'SeasonSegment8'

date_from = 'DateFrom6'

date_to = 'DateTo0'

opponent_team_id = 'OpponentTeamID6'

vs_conference = 'VsConference6'

vs_division = 'VsDivision6'

game_segment = 'GameSegment6'

period = 'Period2'

last_n_games = 'LastNGames4'

client_controller.leaguedashplayerclutch_get(
  clutch_time,
  ahead_behind,
  point_diff,
  game_scope,
  player_experience,
  player_position,
  starter_bench,
  measure_type,
  per_mode,
  plus_minus,
  pace_adjust,
  rank,
  season,
  season_type,
  outcome,
  location,
  month,
  season_segment,
  date_from,
  date_to,
  opponent_team_id,
  vs_conference,
  vs_division,
  game_segment,
  period,
  last_n_games
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



