# Get Heartbeat

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldEhlYXJ0YmVhdA

:information_source: **Note** This endpoint does not require authentication.

```python
def get_heartbeat(self)
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type `str`.


# Example Usage

```python
result = health_api.get_heartbeat()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



