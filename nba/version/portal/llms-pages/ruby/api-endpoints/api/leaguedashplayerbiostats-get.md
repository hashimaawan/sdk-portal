# Leaguedashplayerbiostats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJiaW9zdGF0c19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ruby
def leaguedashplayerbiostats_get(per_mode,
                                 league_id,
                                 season,
                                 season_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_mode` | `String` | Query, Required | - |
| `league_id` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
per_mode = 'PerMode6'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

result = client_api.leaguedashplayerbiostats_get(
  per_mode,
  league_id,
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



