# Franchisehistory GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/python/x-redirect/JTI0ZSUyRiUyRkZyYW5jaGlzZWhpc3RvcnlfR0VU

:information_source: **Note** This endpoint does not require authentication.

```python
def franchisehistory_get(self,
                        league_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `league_id` | `str` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```python
league_id = 'LeagueID4'

client_controller.franchisehistory_get(league_id)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `APIException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `APIException` |



