# Get All Floating I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGFsbCUyNTIwRmxvYXRpbmclMjUyMElQcw

Returns all Floating IP objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_floating_i_ps(self,
                         name=None,
                         label_selector=None,
                         sort=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter Floating IPs by their name. The response will only contain the Floating IP matching the specified name. |
| `label_selector` | `str` | Query, Optional | Can be used to filter Floating IPs by labels. The response will only contain Floating IPs matching the label selector. |
| `sort` | [`Sort2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `floating_ips` key in the reply contains an array of Floating IP objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FloatingIpsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ips-response.md).


# Example Usage

```python
result = floating_i_ps_api.get_all_floating_i_ps()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



