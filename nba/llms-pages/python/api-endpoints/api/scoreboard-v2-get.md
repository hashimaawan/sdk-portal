# Scoreboard V2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRWMl9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def scoreboard_v_2_get(self,
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

`void`


# Example Usage

```python
game_date = 'GameDate8'

league_id = 'LeagueID4'

day_offset = 'DayOffset6'

client_controller.scoreboard_v_2_get(
    game_date,
    league_id,
    day_offset
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



