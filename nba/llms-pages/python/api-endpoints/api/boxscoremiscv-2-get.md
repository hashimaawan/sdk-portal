# Boxscoremiscv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/python/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlbWlzY3YyX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```python
def boxscoremiscv_2_get(self,
                       game_id,
                       start_period,
                       end_period,
                       start_range,
                       end_range,
                       range_type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `game_id` | `str` | Query, Required | - |
| `start_period` | `str` | Query, Required | - |
| `end_period` | `str` | Query, Required | - |
| `start_range` | `str` | Query, Required | - |
| `end_range` | `str` | Query, Required | - |
| `range_type` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
game_id = 'GameID8'

start_period = 'StartPeriod4'

end_period = 'EndPeriod0'

start_range = 'StartRange0'

end_range = 'EndRange2'

range_type = 'RangeType0'

client_controller.boxscoremiscv_2_get(
    game_id,
    start_period,
    end_period,
    start_range,
    end_range,
    range_type
)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



