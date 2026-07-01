# Create a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGQ3JlYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Creates a new PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```python
def create_a_placement_group(self,
                            body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/create-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `PlacementGroup` key contains the PlacementGroup that was just created.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`CreatePlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/create-placement-group-response.md).


# Example Usage

```python
body = CreatePlacementGroupRequest(
    name='my Placement Group'
)

result = placement_groups_api.create_a_placement_group(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "placement_group": {
    "created": "2019-01-08T12:10:00+00:00",
    "id": 897,
    "labels": {
      "key": "value"
    },
    "name": "my Placement Group",
    "servers": [],
    "type": "spread"
  }
}
```



