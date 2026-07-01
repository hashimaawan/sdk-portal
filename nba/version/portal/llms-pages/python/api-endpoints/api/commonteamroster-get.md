# Commonteamroster GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnRlYW1yb3N0ZXJfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def commonteamroster_get(self,
                        season,
                        team_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `str` | Query, Required | - |
| `team_id` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
season = 'Season0'

team_id = 'TeamID8'

client_controller.commonteamroster_get(
    season,
    team_id
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



