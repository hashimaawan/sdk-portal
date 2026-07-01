# Get All Volumes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGFsbCUyNTIwVm9sdW1lcw

Gets all existing Volumes that you have available.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_volumes(self,
                   status=None,
                   sort=None,
                   name=None,
                   label_selector=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Volumes matching the status. |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `str` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `str` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `volumes` key contains a list of volumes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`VolumesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/volumes-response.md).


# Example Usage

```python
result = volumes_api.get_all_volumes()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



