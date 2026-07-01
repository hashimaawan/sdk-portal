# Get All Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwVHlwZXMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVyJTI1MjBUeXBlcw

Gets all Server type objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_server_types(self,
                        name=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter Server types by their name. The response will only contain the Server type matching the specified name. |


# Response Type

**200**: The `server_types` key in the reply contains an array of Server type objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ServerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-types-response.md).


# Example Usage

```python
result = server_types_api.get_all_server_types()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



