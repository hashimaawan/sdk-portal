# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`CreateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | - |
| `home_location` | `String` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | - |
| `server` | `Integer` | Optional | Server to assign the Floating IP to |
| `type` | [`Type17Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-17.md) | Required | Floating IP type |


# Example

```ruby
create_floating_ip_request = CreateFloatingIPRequest.new(
  Type17Enum::IPV4,
  'Web Frontend',
  'fsn1',
  { 'labelkey' => 'value' },
  'Web Frontend',
  42
)
```



