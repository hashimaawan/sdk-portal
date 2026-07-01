# Playerdashptpass GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHBhc3NfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def playerdashptpass_get(self,
                        per_mode,
                        season,
                        season_type,
                        player_id,
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
                        last_n_games)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_mode` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `player_id` | `str` | Query, Required | - |
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
| `last_n_games` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
per_mode = 'PerMode6'

season = 'Season0'

season_type = 'SeasonType8'

player_id = 'PlayerID6'

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

last_n_games = 'LastNGames4'

result = client_api.playerdashptpass_get(
    per_mode,
    season,
    season_type,
    player_id,
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
    last_n_games
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



