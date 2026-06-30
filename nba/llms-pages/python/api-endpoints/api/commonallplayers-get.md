# Commonallplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRkNvbW1vbmFsbHBsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def commonallplayers_get(self,
                        league_id,
                        season,
                        is_only_current_season)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `is_only_current_season` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
league_id = 'LeagueID4'

season = 'Season0'

is_only_current_season = 'IsOnlyCurrentSeason6'

client_controller.commonallplayers_get(
    league_id,
    season,
    is_only_current_season
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



