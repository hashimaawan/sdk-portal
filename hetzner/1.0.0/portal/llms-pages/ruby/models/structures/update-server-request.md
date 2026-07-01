# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New name to set |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_server_request = UpdateServerRequest.new(
  labels: { 'labelkey' => 'value' },
  name: 'my-server',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



