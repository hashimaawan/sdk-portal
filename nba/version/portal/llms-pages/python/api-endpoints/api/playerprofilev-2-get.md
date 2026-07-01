# Playerprofilev 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGV2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```python
def playerprofilev_2_get(self,
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
per_mode = 'PerMode6'

player_id = 'PlayerID6'

result = client_api.playerprofilev_2_get(
    per_mode,
    player_id
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



