# Leaguedashptteamdefend GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwdHRlYW1kZWZlbmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def leaguedashptteamdefend_get(league_id,
                               per_mode,
                               season,
                               season_type,
                               defense_category)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Required | - |
| `per_mode` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
| `defense_category` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
league_id = 'LeagueID4'

per_mode = 'PerMode6'

season = 'Season0'

season_type = 'SeasonType8'

defense_category = 'DefenseCategory0'

result = client_api.leaguedashptteamdefend_get(
  league_id,
  per_mode,
  season,
  season_type,
  defense_category
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



