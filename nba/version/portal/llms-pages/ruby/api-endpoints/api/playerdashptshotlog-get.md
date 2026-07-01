# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ruby
def playerdashptshotlog_get(league_id: nil,
                            season: nil,
                            season_type: nil,
                            player_id: nil,
                            team_id: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `String` | Query, Optional | - |
| `season` | `String` | Query, Optional | - |
| `season_type` | `String` | Query, Optional | - |
| `player_id` | `String` | Query, Optional | - |
| `team_id` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
client_controller.playerdashptshotlog_get
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



