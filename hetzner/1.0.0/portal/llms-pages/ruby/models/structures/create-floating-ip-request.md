# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`CreateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | - |
| `home_location` | `String` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | - |
| `server` | `Integer` | Optional | Server to assign the Floating IP to |
| `type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-17.md) | Required | Floating IP type |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_floating_ip_request = CreateFloatingIpRequest.new(
  type: Type17::IPV4,
  description: 'Web Frontend',
  home_location: 'fsn1',
  labels: { 'labelkey' => 'value' },
  name: 'Web Frontend',
  server: 42,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



