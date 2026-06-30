# Playlists Followers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwRm9sbG93ZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistsFollowersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `public` | `TrueClass \| FalseClass` | Optional | Defaults to `true`. If `true` the playlist will be included in user's public playlists, if `false` it will remain private. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlists_followers_request = PlaylistsFollowersRequest.new(
  public: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



