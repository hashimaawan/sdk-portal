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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
per_mode = 'PerMode6'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

result = client_api.leaguedashplayerbiostats_get(
    per_mode,
    league_id,
    season,
    season_type
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



