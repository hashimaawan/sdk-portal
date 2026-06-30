# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```python
def playerdashptreboundlogs_get(self,
                               season=None,
                               season_type=None,
                               player_id=None,
                               team_id=None,
                               outcome=None,
                               location=None,
                               month=None,
                               season_segment=None,
                               date_from=None,
                               date_to=None,
                               opponent_team_id=None,
                               vs_conference=None,
                               vs_division=None,
                               game_segment=None,
                               period=None,
                               last_n_games=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `str` | Query, Optional | - |
| `season_type` | `str` | Query, Optional | - |
| `player_id` | `str` | Query, Optional | - |
| `team_id` | `str` | Query, Optional | - |
| `outcome` | `str` | Query, Optional | - |
| `location` | `str` | Query, Optional | - |
| `month` | `str` | Query, Optional | - |
| `season_segment` | `str` | Query, Optional | - |
| `date_from` | `str` | Query, Optional | - |
| `date_to` | `str` | Query, Optional | - |
| `opponent_team_id` | `str` | Query, Optional | - |
| `vs_conference` | `str` | Query, Optional | - |
| `vs_division` | `str` | Query, Optional | - |
| `game_segment` | `str` | Query, Optional | - |
| `period` | `str` | Query, Optional | - |
| `last_n_games` | `str` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
client_controller.playerdashptreboundlogs_get()
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



