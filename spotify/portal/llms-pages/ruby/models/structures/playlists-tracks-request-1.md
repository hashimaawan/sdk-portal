# Playlists Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwVHJhY2tzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistsTracksRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uris` | `Array[String]` | Optional | - |
| `range_start` | `Integer` | Optional | The position of the first item to be reordered. |
| `insert_before` | `Integer` | Optional | The position where the items should be inserted.<br/>To reorder the items to the end of the playlist, simply set _insert_before_ to the position after the last item.<br/>Examples:<br/>To reorder the first item to the last position in a playlist with 10 items, set _range_start_ to 0, and _insert_before_ to 10.<br/>To reorder the last item in a playlist with 10 items to the start of the playlist, set _range_start_ to 9, and _insert_before_ to 0. |
| `range_length` | `Integer` | Optional | The amount of items to be reordered. Defaults to 1 if not set.<br/>The range of items to be reordered begins from the _range_start_ position, and includes the _range_length_ subsequent items.<br/>Example:<br/>To move the items at index 9-10 to the start of the playlist, _range_start_ is set to 9, and _range_length_ is set to 2. |
| `snapshot_id` | `String` | Optional | The playlist's snapshot ID against which you want to make the changes. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlists_tracks_request1 = PlaylistsTracksRequest1.new(
  uris: [
    'uris3',
    'uris4',
    'uris5'
  ],
  range_start: 1,
  insert_before: 3,
  range_length: 2,
  snapshot_id: 'snapshot_id2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



