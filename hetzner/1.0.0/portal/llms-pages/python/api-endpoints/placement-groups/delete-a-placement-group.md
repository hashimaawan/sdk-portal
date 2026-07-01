# Delete a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGRGVsZXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Deletes a PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_placement_group(self,
                            id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: PlacementGroup deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
id = 112

result = placement_groups_api.delete_a_placement_group(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



