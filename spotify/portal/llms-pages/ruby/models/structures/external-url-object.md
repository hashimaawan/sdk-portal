# External Url Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkV4dGVybmFsVXJsT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ExternalUrlObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `spotify` | `String` | Optional | The [Spotify URL](/documentation/web-api/concepts/spotify-uris-ids) for the object. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
external_url_object = ExternalUrlObject.new(
  spotify: 'spotify4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



