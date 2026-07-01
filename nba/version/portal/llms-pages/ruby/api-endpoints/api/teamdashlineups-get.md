# Teamdashlineups GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlRlYW1kYXNobGluZXVwc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ruby
def teamdashlineups_get(group_quantity,
                        game_id,
                        season_type,
                        team_id,
                        measure_type,
                        per_mode,
                        plus_minus,
                        pace_adjust,
                        rank,
                        season,
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
| `group_quantity` | `String` | Query, Required | - |
| `game_id` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
| `team_id` | `String` | Query, Required | - |
| `measure_type` | `String` | Query, Required | - |
| `per_mode` | `String` | Query, Required | - |
| `plus_minus` | `String` | Query, Required | - |
| `pace_adjust` | `String` | Query, Required | - |
| `rank` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
group_quantity = 'GroupQuantity0'

game_id = 'GameID8'

season_type = 'SeasonType8'

team_id = 'TeamID8'

measure_type = 'MeasureType8'

per_mode = 'PerMode6'

plus_minus = 'PlusMinus0'

pace_adjust = 'PaceAdjust2'

rank = 'Rank2'

season = 'Season0'

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

result = client_api.teamdashlineups_get(
  group_quantity,
  game_id,
  season_type,
  team_id,
  measure_type,
  per_mode,
  plus_minus,
  pace_adjust,
  rank,
  season,
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



