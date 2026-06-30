# Image Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkltYWdlT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ImageObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `String` | Required | The source URL of the image. |
| `height` | `Integer` | Required | The image height in pixels. |
| `width` | `Integer` | Required | The image width in pixels. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
image_object = ImageObject.new(
  url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
  height: 300,
  width: 300,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



