# Playercareerstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXllcmNhcmVlcnN0YXRzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```python
def playercareerstats_get(self,
                         per_mode,
                         player_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_mode` | `str` | Query, Required | - |
| `player_id` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
per_mode = 'PerMode6'

player_id = 'PlayerID6'

client_controller.playercareerstats_get(
    per_mode,
    player_id
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



