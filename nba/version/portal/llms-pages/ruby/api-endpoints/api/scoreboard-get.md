# Scoreboard GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def scoreboard_get(game_date,
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
game_date = 'GameDate8'

league_id = 'LeagueID4'

day_offset = 'DayOffset6'

result = client_api.scoreboard_get(
  game_date,
  league_id,
  day_offset
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



