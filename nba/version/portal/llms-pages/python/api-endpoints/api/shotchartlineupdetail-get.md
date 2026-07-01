# Shotchartlineupdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGxpbmV1cGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def shotchartlineupdetail_get(self,
                             league_id,
                             season,
                             season_type,
                             team_id,
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
                             last_n_games,
                             game_id,
                             group_id,
                             context_measure,
                             context_filter)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `team_id` | `str` | Query, Required | - |
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
| `game_id` | `str` | Query, Required | - |
| `group_id` | `str` | Query, Required | - |
| `context_measure` | `str` | Query, Required | - |
| `context_filter` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

team_id = 'TeamID8'

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

game_id = 'GameID8'

group_id = 'GROUP_ID6'

context_measure = 'ContextMeasure2'

context_filter = 'ContextFilter6'

result = client_api.shotchartlineupdetail_get(
    league_id,
    season,
    season_type,
    team_id,
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
    last_n_games,
    game_id,
    group_id,
    context_measure,
    context_filter
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



