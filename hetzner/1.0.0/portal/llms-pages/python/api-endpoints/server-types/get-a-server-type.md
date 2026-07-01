# Get a Server Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwVHlwZXMlMkZHZXQlMjUyMGElMjUyMFNlcnZlciUyNTIwVHlwZQ

Gets a specific Server type object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_server_type(self,
                     id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Server Type |


# Response Type

**200**: The `server_type` key in the reply contains a Server type object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ServerTypesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-types-response-1.md).


# Example Usage

```python
id = 112

result = server_types_api.get_a_server_type(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



