# Leaguedashplayerstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJzdGF0c19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def leaguedashplayerstats_get(self,
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
| `game_scope` | `str` | Query, Required | - |
| `player_experience` | `str` | Query, Required | - |
| `player_position` | `str` | Query, Required | - |
| `starter_bench` | `str` | Query, Required | - |
| `measure_type` | `str` | Query, Required | - |
| `per_mode` | `str` | Query, Required | - |
| `plus_minus` | `str` | Query, Required | - |
| `pace_adjust` | `str` | Query, Required | - |
| `rank` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `outcome` | `str` | Query, Required | - |
| `location` | `str` | Query, Required | - |
| `month` | `str` | Query, Required | - |
| `season_segment` | `str` | Query, Required | - |
| `date_from` | `str` | Query, Required | - |
| `date_to` | `str` | Query, Required | - |
| `opponent_team_id` | `str` | Query, Required | - |
| `vs_conference` | `str` | Query, Required | - |
| `vs_division` | `str` | Query, Required | - |
| `game_segment` | `str` | Query, Required | - |
| `period` | `str` | Query, Required | - |
| `last_n_games` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
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

client_controller.leaguedashplayerstats_get(
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



