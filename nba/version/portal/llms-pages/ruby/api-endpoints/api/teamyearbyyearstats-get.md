# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def teamyearbyyearstats_get(league_id,
                            season_type,
                            per_mode,
                            team_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
| `per_mode` | `String` | Query, Required | - |
| `team_id` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
league_id = 'LeagueID4'

season_type = 'SeasonType8'

per_mode = 'PerMode6'

team_id = 'TeamID8'

result = client_api.teamyearbyyearstats_get(
  league_id,
  season_type,
  per_mode,
  team_id
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



