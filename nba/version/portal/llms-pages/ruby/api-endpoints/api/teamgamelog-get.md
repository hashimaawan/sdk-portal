# Teamgamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlRlYW1nYW1lbG9nX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def teamgamelog_get(team_id,
                    season,
                    season_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `team_id` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
team_id = 'TeamID8'

season = 'Season0'

season_type = 'SeasonType8'

result = client_api.teamgamelog_get(
  team_id,
  season,
  season_type
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



