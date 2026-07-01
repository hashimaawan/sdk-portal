# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placement_group` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/placement-group.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
placement_group_response = PlacementGroupResponse.new(
  placement_group: PlacementGroup.new(
    created: '2016-01-30T23:55:00+00:00',
    id: 42,
    labels: {
      'key0' => 'labels4'
    },
    name: 'my-resource',
    servers: [
      42
    ],
    type: 'spread',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



