# Boxscoresummaryv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkJveHNjb3Jlc3VtbWFyeXYyX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def boxscoresummaryv2_get(game_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_id` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
game_id = 'GameID8'

result = client_api.boxscoresummaryv2_get(game_id)

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



