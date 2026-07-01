# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```python
def teaminfocommon_get(self,
                      season,
                      team_id,
                      league_id,
                      season_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `str` | Query, Required | - |
| `team_id` | `str` | Query, Required | - |
| `league_id` | `str` | Query, Required | - |
| `season_type` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
season = 'Season0'

team_id = 'TeamID8'

league_id = 'LeagueID4'

season_type = 'SeasonType8'

client_controller.teaminfocommon_get(
    season,
    team_id,
    league_id,
    season_type
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



