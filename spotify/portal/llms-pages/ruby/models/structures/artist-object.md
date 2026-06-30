# Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkFydGlzdE9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`ArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `followers` | [`FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/followers-object.md) | Optional | Information about the followers of the artist. |
| `genres` | `Array[String]` | Optional | A list of the genres the artist is associated with. If not yet classified, the array is empty. |
| `href` | `String` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `id` | `String` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/image-object.md) | Optional | Images of the artist in various sizes, widest first. |
| `name` | `String` | Optional | The name of the artist. |
| `popularity` | `Integer` | Optional | The popularity of the artist. The value will be between 0 and 100, with 100 being the most popular. The artist's popularity is calculated from the popularity of all the artist's tracks. |
| `type` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/enumerations/type.md) | Optional | The object type. |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
artist_object = ArtistObject.new(
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  followers: FollowersObject.new(
    href: 'href0',
    total: 82,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  genres: [
    'Prog rock',
    'Grunge'
  ],
  href: 'href8',
  id: 'id6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



