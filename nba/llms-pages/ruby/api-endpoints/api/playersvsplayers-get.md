# Playersvsplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/ruby/x-redirect/JTI0ZSUyRiUyRlBsYXllcnN2c3BsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def playersvsplayers_get(player_team_id,
                         player_id1,
                         player_id2,
                         player_id3,
                         player_id4,
                         player_id5,
                         vs_team_id,
                         vs_player_id1,
                         vs_player_id2,
                         vs_player_id3,
                         vs_player_id4,
                         vs_player_id5,
                         season_type,
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
| `player_team_id` | `String` | Query, Required | - |
| `player_id_1` | `String` | Query, Required | - |
| `player_id_2` | `String` | Query, Required | - |
| `player_id_3` | `String` | Query, Required | - |
| `player_id_4` | `String` | Query, Required | - |
| `player_id_5` | `String` | Query, Required | - |
| `vs_team_id` | `String` | Query, Required | - |
| `vs_player_id_1` | `String` | Query, Required | - |
| `vs_player_id_2` | `String` | Query, Required | - |
| `vs_player_id_3` | `String` | Query, Required | - |
| `vs_player_id_4` | `String` | Query, Required | - |
| `vs_player_id_5` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
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

`void`


# Example Usage

```ruby
player_team_id = 'PlayerTeamID4'

player_id1 = 'PlayerID18'

player_id2 = 'PlayerID24'

player_id3 = 'PlayerID32'

player_id4 = 'PlayerID44'

player_id5 = 'PlayerID54'

vs_team_id = 'VsTeamID8'

vs_player_id1 = 'VsPlayerID12'

vs_player_id2 = 'VsPlayerID28'

vs_player_id3 = 'VsPlayerID38'

vs_player_id4 = 'VsPlayerID46'

vs_player_id5 = 'VsPlayerID56'

season_type = 'SeasonType8'

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

client_controller.playersvsplayers_get(
  player_team_id,
  player_id1,
  player_id2,
  player_id3,
  player_id4,
  player_id5,
  vs_team_id,
  vs_player_id1,
  vs_player_id2,
  vs_player_id3,
  vs_player_id4,
  vs_player_id5,
  season_type,
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
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



