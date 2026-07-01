# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/nullable-action.md) | Optional | - |
| `placement_group` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/placement-group.md) | Required | - |


# Example

```ruby
create_placement_group_response = CreatePlacementGroupResponse.new(
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
  ),
  NullableAction.new(
    'command6',
    Error.new(
      'code2',
      'message4'
    ),
    'finished0',
    238,
    143.26,
    [
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      )
    ],
    'started8',
    StatusEnum::RUNNING
  )
)
```



