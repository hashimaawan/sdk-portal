# Get All Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhbGwlMjUyME5ldHdvcmtz

Gets all existing networks that you have available.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_networks(self,
                    name=None,
                    label_selector=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter networks by their name. The response will only contain the networks matching the specified name. |
| `label_selector` | `str` | Query, Optional | Can be used to filter networks by labels. The response will only contain networks with a matching label selector pattern. |


# Response Type

**200**: The `networks` key contains a list of networks

[`NetworksResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/networks-response.md)


# Example Usage

```python
result = networks_controller.get_all_networks()
print(result)
```



