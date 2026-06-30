# Playlists Tracks Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwVHJhY2tzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistsTracksRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tracks` | [`Array[Track1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/track-1.md) | Required | An array of objects containing [Spotify URIs](/documentation/web-api/concepts/spotify-uris-ids) of the tracks or episodes to remove.<br>For example: `{ "tracks": [{ "uri": "spotify:track:4iV5W9uYEdYUVa79Axb7Rh" },{ "uri": "spotify:track:1301WleyT98MSxVHPZCA6M" }] }`. A maximum of 100 objects can be sent at once. |
| `snapshot_id` | `String` | Optional | The playlist's snapshot ID against which you want to make the changes.<br>The API will validate that the specified items exist and in the specified positions and make the changes,<br>even if more recent changes have been made to the playlist. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlists_tracks_request2 = PlaylistsTracksRequest2.new(
  tracks: [
    Track1.new(
      uri: 'uri8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  snapshot_id: 'snapshot_id8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



