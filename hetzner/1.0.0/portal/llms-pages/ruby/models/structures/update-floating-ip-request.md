# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`UpdateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | New Description to set |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New unique name to set |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_floating_ip_request = UpdateFloatingIpRequest.new(
  description: 'Web Frontend',
  labels: { 'labelkey' => 'value' },
  name: 'Web Frontend',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



