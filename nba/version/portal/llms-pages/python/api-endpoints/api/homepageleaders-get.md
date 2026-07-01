# Homepageleaders GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdlbGVhZGVyc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def homepageleaders_get(self,
                       stat_category,
                       league_id,
                       season,
                       season_type,
                       player_or_team,
                       player_scope,
                       game_scope,
                       game=None,
                       player=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stat_category` | `str` | Query, Required | - |
| `league_id` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `player_or_team` | `str` | Query, Required | - |
| `player_scope` | `str` | Query, Required | - |
| `game_scope` | `str` | Query, Required | - |
| `game` | `str` | Query, Optional | - |
| `player` | `str` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
stat_category = 'StatCategory6'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

player_or_team = 'PlayerOrTeam8'

player_scope = 'PlayerScope2'

game_scope = 'GameScope0'

result = client_api.homepageleaders_get(
    stat_category,
    league_id,
    season,
    season_type,
    player_or_team,
    player_scope,
    game_scope
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



