# Private User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlByaXZhdGVVc2VyT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PrivateUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `country` | `String` | Optional | The country of the user, as set in the user's account profile. An [ISO 3166-1 alpha-2 country code](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _This field is only available when the current user has granted access to the [user-read-private](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `display_name` | `String` | Optional | The name displayed on the user's profile. `null` if not available. |
| `email` | `String` | Optional | The user's email address, as entered by the user when creating their account. _**Important!** This email address is unverified; there is no proof that it actually belongs to the user._ _This field is only available when the current user has granted access to the [user-read-email](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `explicit_content` | [`ExplicitContentSettingsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/explicit-content-settings-object.md) | Optional | The user's explicit content settings. _This field is only available when the current user has granted access to the [user-read-private](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | Known external URLs for this user. |
| `followers` | [`FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/followers-object.md) | Optional | Information about the followers of the user. |
| `href` | `String` | Optional | A link to the Web API endpoint for this user. |
| `id` | `String` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for the user. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/image-object.md) | Optional | The user's profile image. |
| `product` | `String` | Optional | The user's Spotify subscription level: "premium", "free", etc. (The subscription level "open" can be considered the same as "free".) _This field is only available when the current user has granted access to the [user-read-private](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `type` | `String` | Optional | The object type: "user" |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the user. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
private_user_object = PrivateUserObject.new(
  country: 'country8',
  display_name: 'display_name4',
  email: 'email2',
  explicit_content: ExplicitContentSettingsObject.new(
    filter_enabled: false,
    filter_locked: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



