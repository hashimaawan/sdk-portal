# Linked Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkxpbmtlZFRyYWNrT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`LinkedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/external-url-object.md) | Optional | Known external URLs for this track. |
| `href` | `String` | Optional | A link to the Web API endpoint providing full details of the track. |
| `id` | `String` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `type` | `String` | Optional | The object type: "track". |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
linked_track_object = LinkedTrackObject.new(
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  href: 'href0',
  id: 'id8',
  type: 'type2',
  uri: 'uri2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



