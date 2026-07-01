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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
id = 112

result = placement_groups_api.delete_a_placement_group(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



