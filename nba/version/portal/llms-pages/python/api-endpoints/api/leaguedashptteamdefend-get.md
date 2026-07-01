# Leaguedashptteamdefend GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwdHRlYW1kZWZlbmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def leaguedashptteamdefend_get(self,
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
league_id = 'LeagueID4'

per_mode = 'PerMode6'

season = 'Season0'

season_type = 'SeasonType8'

defense_category = 'DefenseCategory0'

result = client_api.leaguedashptteamdefend_get(
    league_id,
    per_mode,
    season,
    season_type,
    defense_category
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



