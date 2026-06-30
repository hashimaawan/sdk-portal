# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`UpdatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_delete` | `TrueClass \| FalseClass` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New unique name to set |


# Example

```ruby
update_primary_ip_request = UpdatePrimaryIPRequest.new(
  true,
  { 'labelkey' => 'value' },
  'my-ip'
)
```



