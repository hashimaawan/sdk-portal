# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placement_group` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/placement-group.md) | Required | - |


# Example

```ruby
placement_group_response = PlacementGroupResponse.new(
  PlacementGroup.new(
    '2016-01-30T23:55:00+00:00',
    42,
    {
      'key0': 'labels4'
    },
    'my-resource',
    [
      42
    ],
    'spread'
  )
)
```



