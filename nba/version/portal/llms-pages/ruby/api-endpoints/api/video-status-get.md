# Video Status GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlZpZGVvU3RhdHVzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def video_status_get(league_id,
                     game_date)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Required | - |
| `game_date` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
league_id = 'LeagueID4'

game_date = 'GameDate8'

result = client_api.video_status_get(
  league_id,
  game_date
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



