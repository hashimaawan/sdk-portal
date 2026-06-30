# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def teamyearbyyearstats_get(self,
                           league_id,
                           season_type,
                           per_mode,
                           team_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `per_mode` | `str` | Query, Required | - |
| `team_id` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
league_id = 'LeagueID4'

season_type = 'SeasonType8'

per_mode = 'PerMode6'

team_id = 'TeamID8'

client_controller.teamyearbyyearstats_get(
    league_id,
    season_type,
    per_mode,
    team_id
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



