# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_delete` | `TrueClass \| FalseClass` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New unique name to set |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_primary_ip_request = UpdatePrimaryIpRequest.new(
  auto_delete: true,
  labels: { 'labelkey' => 'value' },
  name: 'my-ip',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



