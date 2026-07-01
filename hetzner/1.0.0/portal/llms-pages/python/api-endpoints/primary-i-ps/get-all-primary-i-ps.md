# Get All Primary I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYWxsJTI1MjBQcmltYXJ5JTI1MjBJUHM

Returns all Primary IP objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_primary_i_ps(self,
                        name=None,
                        label_selector=None,
                        ip=None,
                        sort=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `str` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `ip` | `str` | Query, Optional | Can be used to filter resources by their ip. The response will only contain the resources matching the specified ip. |
| `sort` | [`Sort2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `primary_ips` key contains an array of Primary IP objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`PrimaryIPsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/primary-i-ps-response.md).


# Example Usage

```python
ip = '127.0.0.1'

result = primary_i_ps_api.get_all_primary_i_ps(
    ip=ip
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



