# Get All Servers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVycw

Returns all existing Server objects

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_servers(self,
                   name=None,
                   label_selector=None,
                   sort=None,
                   status=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `str` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status70`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-70.md) | Query, Optional | Can be used multiple times. The response will only contain Server matching the status |


# Response Type

**200**: A paged array of servers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ServersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-response.md).


# Example Usage

```python
result = servers_api.get_all_servers()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



