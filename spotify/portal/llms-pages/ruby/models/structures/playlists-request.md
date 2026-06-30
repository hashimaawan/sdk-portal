# Playlists Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | The new name for the playlist, for example `"My New Playlist Title"` |
| `public` | `TrueClass \| FalseClass` | Optional | If `true` the playlist will be public, if `false` it will be private. |
| `collaborative` | `TrueClass \| FalseClass` | Optional | If `true`, the playlist will become collaborative and other users will be able to modify the playlist in their Spotify client. <br/><br>_**Note**: You can only set `collaborative` to `true` on non-public playlists._ |
| `description` | `String` | Optional | Value for playlist description as displayed in Spotify Clients and in the Web API. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlists_request = PlaylistsRequest.new(
  name: 'Updated Playlist Name',
  public: false,
  collaborative: false,
  description: 'Updated playlist description',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



