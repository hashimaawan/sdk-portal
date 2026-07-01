# Boxscorescoring GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkJveHNjb3Jlc2NvcmluZ19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def boxscorescoring_get(self,
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
result = client_api.boxscorescoring_get()

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



