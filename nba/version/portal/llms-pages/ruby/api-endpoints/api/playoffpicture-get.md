# Playoffpicture GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlBsYXlvZmZwaWN0dXJlX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def playoffpicture_get(league_id,
                       season_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Required | - |
| `season_id` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
league_id = 'LeagueID4'

season_id = 'SeasonID6'

client_controller.playoffpicture_get(
  league_id,
  season_id
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



