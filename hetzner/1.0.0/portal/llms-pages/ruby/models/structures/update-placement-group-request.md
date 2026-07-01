# Update Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`UpdatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New PlacementGroup name |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_placement_group_request = UpdatePlacementGroupRequest.new(
  labels: { 'labelkey' => 'value' },
  name: 'my Placement Group',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



