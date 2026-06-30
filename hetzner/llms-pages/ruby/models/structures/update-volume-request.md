# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | New Volume name |


# Example

```ruby
update_volume_request = UpdateVolumeRequest.new(
  'database-storage',
  Labels2.new(
    'labelkey4'
  )
)
```



