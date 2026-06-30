# Playlist Tracks Ref Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tzUmVmT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistTracksRefObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Optional | A link to the Web API endpoint where full details of the playlist's tracks can be retrieved. |
| `total` | `Integer` | Optional | Number of tracks in the playlist. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlist_tracks_ref_object = PlaylistTracksRefObject.new(
  href: 'href8',
  total: 22,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



