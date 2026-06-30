# Public User Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlB1YmxpY1VzZXJPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PublicUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `display_name` | `String` | Optional | The name displayed on the user's profile. `null` if not available. |
| `external_urls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `followers` | [`FollowersObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `href` | `String` | Optional | A link to the Web API endpoint for this user. |
| `id` | `String` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `images` | [`Array[ImageObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/image-object.md) | Optional | The user's profile image. |
| `type` | [`Type3`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/enumerations/type-3.md) | Optional | The object type. |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
public_user_object = PublicUserObject.new(
  display_name: 'display_name8',
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
  href: 'href0',
  id: 'id8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



