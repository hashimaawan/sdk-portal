# Draftcombinedrillresults GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkRyYWZ0Y29tYmluZWRyaWxscmVzdWx0c19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```ruby
def draftcombinedrillresults_get(league_id,
                                 season_year)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Required | - |
| `season_year` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
league_id = 'LeagueID4'

season_year = 'SeasonYear6'

result = client_api.draftcombinedrillresults_get(
  league_id,
  season_year
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



