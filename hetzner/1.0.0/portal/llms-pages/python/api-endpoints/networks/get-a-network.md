# Get a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhJTI1MjBOZXR3b3Jr

Gets a specific network object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_network(self,
                 id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the network |


# Response Type

**200**: The `network` key contains the network

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`NetworksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/networks-response-1.md).


# Example Usage

```python
id = 112

result = networks_api.get_a_network(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



