# Draftcombinedrillresults GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/ruby/x-redirect/JTI0ZSUyRiUyRkRyYWZ0Y29tYmluZWRyaWxscmVzdWx0c19HRVQ

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

`void`


# Example Usage

```ruby
league_id = 'LeagueID4'

season_year = 'SeasonYear6'

client_controller.draftcombinedrillresults_get(
  league_id,
  season_year
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



