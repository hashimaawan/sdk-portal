# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | Description of the Image, will be auto-generated if not set |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type63Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |


# Example

```ruby
create_image_request = CreateImageRequest.new(
  'my image',
  Labels.new(
    'labelkey4'
  ),
  Type63Enum::SNAPSHOT
)
```



