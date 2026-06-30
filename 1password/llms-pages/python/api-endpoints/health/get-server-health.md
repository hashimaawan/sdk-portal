# Get Server Health

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldFNlcnZlckhlYWx0aA

:information_source: **Note** This endpoint does not require authentication.

```python
def get_server_health(self)
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`HealthResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/health-response.md).


# Example Usage

```python
result = health_api.get_server_health()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "dependencies": [
    {
      "service": "sync",
      "status": "TOKEN_NEEDED"
    },
    {
      "message": "Connected to./1password.sqlite",
      "service": "sqlite",
      "status": "ACTIVE"
    }
  ],
  "name": "1Password Connect API",
  "version": "1.2.1"
}
```



