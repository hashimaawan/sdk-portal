# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | Description of the Image, will be auto-generated if not set |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type63`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_image_request = CreateImageRequest.new(
  description: 'my image',
  labels: Labels.new(
    labelkey: 'labelkey4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: Type63::SNAPSHOT,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



