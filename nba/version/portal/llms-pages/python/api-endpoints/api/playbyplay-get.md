# Playbyplay GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXlieXBsYXlfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def playbyplay_get(self,
                  game_id,
                  start_period,
                  end_period)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_id` | `str` | Query, Required | - |
| `start_period` | `str` | Query, Required | - |
| `end_period` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
game_id = 'GameID8'

start_period = 'StartPeriod4'

end_period = 'EndPeriod0'

result = client_api.playbyplay_get(
    game_id,
    start_period,
    end_period
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



