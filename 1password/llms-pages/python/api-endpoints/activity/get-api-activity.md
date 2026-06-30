# Get Api Activity

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkFjdGl2aXR5JTJGR2V0QXBpQWN0aXZpdHk

```python
def get_api_activity(self,
                    limit=50,
                    offset=0)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int` | Query, Optional | How many API Events should be retrieved in a single request.<br><br>**Default**: `50` |
| `offset` | `int` | Query, Optional | How far into the collection of API Events should the response start<br><br>**Default**: `0` |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`List[ApiRequest]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/api-request.md).


# Example Usage

```python
limit = 10

offset = 50

result = activity_api.get_api_activity(
    limit=limit,
    offset=offset
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |



