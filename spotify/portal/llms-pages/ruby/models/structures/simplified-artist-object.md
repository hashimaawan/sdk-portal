# Simplified Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`SimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_urls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `href` | `String` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `id` | `String` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `name` | `String` | Optional | The name of the artist. |
| `type` | [`Type`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/enumerations/type.md) | Optional | The object type. |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
simplified_artist_object = SimplifiedArtistObject.new(
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  href: 'href6',
  id: 'id4',
  name: 'name4',
  type: Type::ARTIST,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



