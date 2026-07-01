# Delete a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGRGVsZXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Deletes a PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_placement_group(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |


# Response Type

**204**: PlacementGroup deleted

`void`


# Example Usage

```ruby
id = 112

placement_groups_controller.delete_a_placement_group(id)
```



