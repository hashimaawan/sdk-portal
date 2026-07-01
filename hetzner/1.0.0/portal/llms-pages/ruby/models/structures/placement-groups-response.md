# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `placement_groups` | [`Array[PlacementGroup]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/placement-group.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
placement_groups_response = PlacementGroupsResponse.new(
  placement_groups: [
    PlacementGroup.new(
      created: '2016-01-30T23:55:00+00:00',
      id: 42,
      labels: {
        'key0' => 'labels0',
        'key1' => 'labels1'
      },
      name: 'my-resource',
      servers: [
        42
      ],
      type: 'spread',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  meta: Meta.new(
    pagination: Pagination.new(
      last_page: 77.7,
      next_page: 209.18,
      page: 17.58,
      per_page: 13.34,
      previous_page: 50.02,
      total_entries: 206.64,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



