# Leaguedashptdefend GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwdGRlZmVuZF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def leaguedashptdefend_get(self,
                          league_id,
                          per_mode,
                          season,
                          season_type,
                          defense_category)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `per_mode` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `defense_category` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
league_id = 'LeagueID4'

per_mode = 'PerMode6'

season = 'Season0'

season_type = 'SeasonType8'

defense_category = 'DefenseCategory0'

client_controller.leaguedashptdefend_get(
    league_id,
    per_mode,
    season,
    season_type,
    defense_category
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



