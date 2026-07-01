# Scoreboard V2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRWMl9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ruby
def scoreboard_v2_get(game_date,
                      league_id,
                      day_offset)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_date` | `String` | Query, Required | - |
| `league_id` | `String` | Query, Required | - |
| `day_offset` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
game_date = 'GameDate8'

league_id = 'LeagueID4'

day_offset = 'DayOffset6'

client_controller.scoreboard_v2_get(
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



