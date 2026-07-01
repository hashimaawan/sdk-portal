# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | New description of Image |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_image_request = UpdateImageRequest.new(
  description: 'My new Image description',
  labels: { 'labelkey' => 'value' },
  type: Type24::SNAPSHOT,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



