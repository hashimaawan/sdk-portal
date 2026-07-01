# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def allstarballotpredictor_get(self,
                              west_player_1,
                              west_player_2,
                              west_player_3,
                              west_player_4,
                              west_player_5,
                              east_player_1,
                              east_player_2,
                              east_player_3,
                              east_player_4,
                              east_player_5,
                              point_cap=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `west_player_1` | `str` | Query, Required | - |
| `west_player_2` | `str` | Query, Required | - |
| `west_player_3` | `str` | Query, Required | - |
| `west_player_4` | `str` | Query, Required | - |
| `west_player_5` | `str` | Query, Required | - |
| `east_player_1` | `str` | Query, Required | - |
| `east_player_2` | `str` | Query, Required | - |
| `east_player_3` | `str` | Query, Required | - |
| `east_player_4` | `str` | Query, Required | - |
| `east_player_5` | `str` | Query, Required | - |
| `point_cap` | `str` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
west_player_1 = 'WestPlayer10'

west_player_2 = 'WestPlayer24'

west_player_3 = 'WestPlayer32'

west_player_4 = 'WestPlayer48'

west_player_5 = 'WestPlayer56'

east_player_1 = 'EastPlayer18'

east_player_2 = 'EastPlayer26'

east_player_3 = 'EastPlayer32'

east_player_4 = 'EastPlayer44'

east_player_5 = 'EastPlayer54'

result = client_api.allstarballotpredictor_get(
    west_player_1,
    west_player_2,
    west_player_3,
    west_player_4,
    west_player_5,
    east_player_1,
    east_player_2,
    east_player_3,
    east_player_4,
    east_player_5
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



