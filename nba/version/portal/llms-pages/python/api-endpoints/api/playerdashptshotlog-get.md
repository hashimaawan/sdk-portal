# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def playerdashptshotlog_get(self,
                           league_id=None,
                           season=None,
                           season_type=None,
                           player_id=None,
                           team_id=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Optional | - |
| `season` | `str` | Query, Optional | - |
| `season_type` | `str` | Query, Optional | - |
| `player_id` | `str` | Query, Optional | - |
| `team_id` | `str` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
client_controller.playerdashptshotlog_get()
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



