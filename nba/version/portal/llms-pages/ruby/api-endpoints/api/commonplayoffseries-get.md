# Commonplayoffseries GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnBsYXlvZmZzZXJpZXNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def commonplayoffseries_get(league_id,
                            season)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
league_id = 'LeagueID4'

season = 'Season0'

client_controller.commonplayoffseries_get(
  league_id,
  season
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



