# Users Playlists Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlVzZXJzJTI1MjBQbGF5bGlzdHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UsersPlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | The name for the new playlist, for example `"Your Coolest Playlist"`. This name does not need to be unique; a user may have several playlists with the same name. |
| `public` | `TrueClass \| FalseClass` | Optional | Defaults to `true`. If `true` the playlist will be public, if `false` it will be private. To be able to create private playlists, the user must have granted the `playlist-modify-private` [scope](/documentation/web-api/concepts/scopes/#list-of-scopes) |
| `collaborative` | `TrueClass \| FalseClass` | Optional | Defaults to `false`. If `true` the playlist will be collaborative. _**Note**: to create a collaborative playlist you must also set `public` to `false`. To create collaborative playlists you must have granted `playlist-modify-private` and `playlist-modify-public` [scopes](/documentation/web-api/concepts/scopes/#list-of-scopes)._ |
| `description` | `String` | Optional | value for playlist description as displayed in Spotify Clients and in the Web API. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
users_playlists_request = UsersPlaylistsRequest.new(
  name: 'New Playlist',
  public: false,
  collaborative: false,
  description: 'New playlist description',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



