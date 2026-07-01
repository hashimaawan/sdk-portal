# Get All Firewalls

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkdldCUyNTIwYWxsJTI1MjBGaXJld2FsbHM

Returns all Firewall objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_firewalls(self,
                     sort=None,
                     name=None,
                     label_selector=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `str` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `str` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `firewalls` key contains an array of Firewall objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FirewallsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/firewalls-response.md).


# Example Usage

```python
result = firewalls_api.get_all_firewalls()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



