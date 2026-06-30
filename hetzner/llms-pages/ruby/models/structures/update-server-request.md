# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New name to set |


# Example

```ruby
update_server_request = UpdateServerRequest.new(
  { 'labelkey' => 'value' },
  'my-server'
)
```



