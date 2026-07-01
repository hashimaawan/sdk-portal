# Teamgamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlRlYW1nYW1lbG9nX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```python
def teamgamelog_get(self,
                   team_id,
                   season,
                   season_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `team_id` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
team_id = 'TeamID8'

season = 'Season0'

season_type = 'SeasonType8'

result = client_api.teamgamelog_get(
    team_id,
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



