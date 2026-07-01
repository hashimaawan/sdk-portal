# Scoreboard GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def scoreboard_get(self,
                  game_date,
                  league_id,
                  day_offset)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_date` | `str` | Query, Required | - |
| `league_id` | `str` | Query, Required | - |
| `day_offset` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
game_date = 'GameDate8'

league_id = 'LeagueID4'

day_offset = 'DayOffset6'

result = client_api.scoreboard_get(
    game_date,
    league_id,
    day_offset
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



