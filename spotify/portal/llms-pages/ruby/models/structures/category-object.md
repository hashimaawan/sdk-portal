# Category Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkNhdGVnb3J5T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`CategoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning full details of the category. |
| `icons` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/image-object.md) | Required | The category icon, in various sizes. |
| `id` | `String` | Required | The [Spotify category ID](/documentation/web-api/concepts/spotify-uris-ids) of the category. |
| `name` | `String` | Required | The name of the category. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
category_object = CategoryObject.new(
  href: 'href6',
  icons: [
    ImageObject.new(
      url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
      height: 300,
      width: 300,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  id: 'equal',
  name: 'EQUAL',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



