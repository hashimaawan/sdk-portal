# Playlist Snapshot Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0U25hcHNob3RJZA

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistSnapshotId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshot_id` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlist_snapshot_id = PlaylistSnapshotId.new(
  snapshot_id: 'abc',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



