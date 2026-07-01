# Teamdashptpass GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlRlYW1kYXNocHRwYXNzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def teamdashptpass_get(per_mode,
                       season,
                       season_type,
                       team_id,
                       outcome,
                       location,
                       month,
                       season_segment,
                       date_from,
                       date_to,
                       opponent_team_id,
                       vs_conference,
                       vs_division,
                       last_n_games)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_mode` | `String` | Query, Required | - |
| `season` | `String` | Query, Required | - |
| `season_type` | `String` | Query, Required | - |
| `team_id` | `String` | Query, Required | - |
| `outcome` | `String` | Query, Required | - |
| `location` | `String` | Query, Required | - |
| `month` | `String` | Query, Required | - |
| `season_segment` | `String` | Query, Required | - |
| `date_from` | `String` | Query, Required | - |
| `date_to` | `String` | Query, Required | - |
| `opponent_team_id` | `String` | Query, Required | - |
| `vs_conference` | `String` | Query, Required | - |
| `vs_division` | `String` | Query, Required | - |
| `last_n_games` | `String` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```ruby
per_mode = 'PerMode6'

season = 'Season0'

season_type = 'SeasonType8'

team_id = 'TeamID8'

outcome = 'Outcome4'

location = 'Location4'

month = 'Month0'

season_segment = 'SeasonSegment8'

date_from = 'DateFrom6'

date_to = 'DateTo0'

opponent_team_id = 'OpponentTeamID6'

vs_conference = 'VsConference6'

vs_division = 'VsDivision6'

last_n_games = 'LastNGames4'

client_controller.teamdashptpass_get(
  per_mode,
  season,
  season_type,
  team_id,
  outcome,
  location,
  month,
  season_segment,
  date_from,
  date_to,
  opponent_team_id,
  vs_conference,
  vs_division,
  last_n_games
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



