# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `placement_groups` | [`Array[PlacementGroup]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/placement-group.md) | Required | - |


# Example

```ruby
placement_groups_response = PlacementGroupsResponse.new(
  [
    PlacementGroup.new(
      '2016-01-30T23:55:00+00:00',
      42,
      {
        'key0': 'labels0',
        'key1': 'labels1'
      },
      'my-resource',
      [
        42
      ],
      'spread'
    )
  ],
  Meta.new(
    Pagination.new(
      77.7,
      209.18,
      17.58,
      13.34,
      50.02,
      206.64
    )
  )
)
```



