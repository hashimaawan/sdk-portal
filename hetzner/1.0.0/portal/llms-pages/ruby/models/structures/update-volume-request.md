# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | New Volume name |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_volume_request = UpdateVolumeRequest.new(
  name: 'database-storage',
  labels: Labels2.new(
    labelkey: 'labelkey4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



