# Get a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGElMjUyMFNlcnZlcg

Returns a specific Server object. The Server must exist inside the Project

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_server(self,
                id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**200**: The `server` key in the reply contains a Server object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-response-2.md).


# Example Usage

```python
id = 112

result = servers_api.get_a_server(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



