# Playlist Owner Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0T3duZXJPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistOwnerObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `followers` | [`FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `href` | `String` | Optional | A link to the Web API endpoint for this user. |
| `id` | `String` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `type` | [`Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/enumerations/type-3.md) | Optional | The object type. |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `display_name` | `String` | Optional | The name displayed on the user's profile. `null` if not available. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlist_owner_object = PlaylistOwnerObject.new(
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
  href: 'href2',
  id: 'id0',
  type: Type3::USER,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



