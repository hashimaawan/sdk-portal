# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def playerdashptreboundlogs_get(season: nil,
                                season_type: nil,
                                player_id: nil,
                                team_id: nil,
                                outcome: nil,
                                location: nil,
                                month: nil,
                                season_segment: nil,
                                date_from: nil,
                                date_to: nil,
                                opponent_team_id: nil,
                                vs_conference: nil,
                                vs_division: nil,
                                game_segment: nil,
                                period: nil,
                                last_n_games: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `String` | Query, Optional | - |
| `season_type` | `String` | Query, Optional | - |
| `player_id` | `String` | Query, Optional | - |
| `team_id` | `String` | Query, Optional | - |
| `outcome` | `String` | Query, Optional | - |
| `location` | `String` | Query, Optional | - |
| `month` | `String` | Query, Optional | - |
| `season_segment` | `String` | Query, Optional | - |
| `date_from` | `String` | Query, Optional | - |
| `date_to` | `String` | Query, Optional | - |
| `opponent_team_id` | `String` | Query, Optional | - |
| `vs_conference` | `String` | Query, Optional | - |
| `vs_division` | `String` | Query, Optional | - |
| `game_segment` | `String` | Query, Optional | - |
| `period` | `String` | Query, Optional | - |
| `last_n_games` | `String` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
result = client_api.playerdashptreboundlogs_get

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



