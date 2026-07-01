# Update a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGVXBkYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Updates the PlacementGroup properties.

Note that when updating labels, the PlacementGroup’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the PlacementGroup object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def update_a_placement_group(id,
                             body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |
| `body` | [`UpdatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/update-placement-group-request.md) | Body, Optional | - |


# Response Type

**200**: The `certificate` key contains the PlacementGroup that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`PlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/placement-group-response.md).


# Example Usage

```ruby
id = 112

body = UpdatePlacementGroupRequest.new(
  labels: { 'labelkey' => 'value' },
  name: 'my Placement Group'
)

result = placement_groups_api.update_a_placement_group(
  id,
  body: body
)

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
    "servers": [
      4711,
      4712
    ],
    "type": "spread"
  }
}
```



