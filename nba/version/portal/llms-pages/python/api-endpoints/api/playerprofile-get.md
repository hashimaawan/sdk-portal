# Playerprofile GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def playerprofile_get(self,
                     league_id,
                     player_id,
                     season,
                     season_type,
                     graph_start_season,
                     graph_end_season,
                     graph_stat)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |
| `player_id` | `str` | Query, Required | - |
| `season` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |
| `graph_start_season` | `str` | Query, Required | - |
| `graph_end_season` | `str` | Query, Required | - |
| `graph_stat` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
league_id = 'LeagueID4'

player_id = 'PlayerID6'

season = 'Season0'

season_type = 'SeasonType8'

graph_start_season = 'GraphStartSeason2'

graph_end_season = 'GraphEndSeason6'

graph_stat = 'GraphStat0'

client_controller.playerprofile_get(
    league_id,
    player_id,
    season,
    season_type,
    graph_start_season,
    graph_end_season,
    graph_stat
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



