# Playoffpicture GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXlvZmZwaWN0dXJlX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```python
def playoffpicture_get(self,
                      league_id,
                      season_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `season_id` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
league_id = 'LeagueID4'

season_id = 'SeasonID6'

result = client_api.playoffpicture_get(
    league_id,
    season_id
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



