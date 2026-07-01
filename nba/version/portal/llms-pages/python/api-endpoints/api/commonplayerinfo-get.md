# Commonplayerinfo GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnBsYXllcmluZm9fR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def commonplayerinfo_get(self,
                        player_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `player_id` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
player_id = 'PlayerID6'

client_controller.commonplayerinfo_get(player_id)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



