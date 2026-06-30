# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | New description of Image |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |


# Example

```ruby
update_image_request = UpdateImageRequest.new(
  'My new Image description',
  { 'labelkey' => 'value' },
  Type24Enum::SNAPSHOT
)
```



