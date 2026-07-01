# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New network name |


# Example

```ruby
update_network_request = UpdateNetworkRequest.new(
  Labels2.new(
    'labelkey4'
  ),
  'new-name'
)
```



