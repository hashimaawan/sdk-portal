# Create a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGQ3JlYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Creates a new PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def create_a_placement_group(body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/create-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `PlacementGroup` key contains the PlacementGroup that was just created.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`CreatePlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/create-placement-group-response.md).


# Example Usage

```ruby
body = CreatePlacementGroupRequest.new(
  name: 'my Placement Group',
  type: 'spread'
)

result = placement_groups_api.create_a_placement_group(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
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



