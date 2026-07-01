# Leaguedashplayerptshot GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJwdHNob3RfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def leaguedashplayerptshot_get(self,
                              league_id,
                              per_mode,
                              season,
                              season_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `per_mode` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
league_id = 'LeagueID4'

per_mode = 'PerMode6'

season = 'Season0'

season_type = 'SeasonType8'

client_controller.leaguedashplayerptshot_get(
    league_id,
    per_mode,
    season,
    season_type
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



