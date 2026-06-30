# Boxscoreadvanced GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlYWR2YW5jZWRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def boxscoreadvanced_get(self,
                        game_id=None,
                        start_period=None,
                        end_period=None,
                        start_range=None,
                        end_range=None,
                        range_type=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_id` | `str` | Query, Optional | - |
| `start_period` | `str` | Query, Optional | - |
| `end_period` | `str` | Query, Optional | - |
| `start_range` | `str` | Query, Optional | - |
| `end_range` | `str` | Query, Optional | - |
| `range_type` | `str` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
client_controller.boxscoreadvanced_get()
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



