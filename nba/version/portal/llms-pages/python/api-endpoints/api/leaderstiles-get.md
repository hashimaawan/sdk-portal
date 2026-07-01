# Leaderstiles GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxlYWRlcnN0aWxlc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def leaderstiles_get(self,
                    stat,
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
| `stat` | `str` | Query, Required | - |
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

`void`


# Example Usage

```python
stat = 'Stat2'

league_id = 'LeagueID4'

season = 'Season0'

season_type = 'SeasonType8'

player_or_team = 'PlayerOrTeam8'

player_scope = 'PlayerScope2'

game_scope = 'GameScope0'

client_controller.leaderstiles_get(
    stat,
    league_id,
    season,
    season_type,
    player_or_team,
    player_scope,
    game_scope
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



