# Leaguedashplayerbiostats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJiaW9zdGF0c19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def leaguedashplayerbiostats_get(self,
                                per_mode,
                                league_id,
                                season,
                                season_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_mode` | `str` | Query, Required | - |
| `league_id` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
per_mode = 'PerMode6'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

client_controller.leaguedashplayerbiostats_get(
    per_mode,
    league_id,
    season,
    season_type
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



