# Simplified Track Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRUcmFja09iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`SimplifiedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`Array[SimplifiedArtistObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/simplified-artist-object.md) | Optional | The artists who performed the track. Each artist object includes a link in `href` to more detailed information about the artist. |
| `available_markets` | `Array[String]` | Optional | A list of the countries in which the track can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `disc_number` | `Integer` | Optional | The disc number (usually `1` unless the album consists of more than one disc). |
| `duration_ms` | `Integer` | Optional | The track length in milliseconds. |
| `explicit` | `TrueClass \| FalseClass` | Optional | Whether or not the track has explicit lyrics ( `true` = yes it does; `false` = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | External URLs for this track. |
| `href` | `String` | Optional | A link to the Web API endpoint providing full details of the track. |
| `id` | `String` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `is_playable` | `TrueClass \| FalseClass` | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking/) is applied. If `true`, the track is playable in the given market. Otherwise `false`. |
| `linked_from` | [`LinkedTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/linked-track-object.md) | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking/) is applied and is only part of the response if the track linking, in fact, exists. The requested track has been replaced with a different track. The track in the `linked_from` object contains information about the originally requested track. |
| `restrictions` | [`TrackRestrictionObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/track-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `name` | `String` | Optional | The name of the track. |
| `preview_url` | `String` | Optional | A URL to a 30 second preview (MP3 format) of the track. |
| `track_number` | `Integer` | Optional | The number of the track. If an album has several discs, the track number is the number on the specified disc. |
| `type` | `String` | Optional | The object type: "track". |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `is_local` | `TrueClass \| FalseClass` | Optional | Whether or not the track is from a local file. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
simplified_track_object = SimplifiedTrackObject.new(
  artists: [
    SimplifiedArtistObject.new(
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href2',
      id: 'id0',
      name: 'name0',
      type: Type::ARTIST,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    SimplifiedArtistObject.new(
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href2',
      id: 'id0',
      name: 'name0',
      type: Type::ARTIST,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    SimplifiedArtistObject.new(
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href2',
      id: 'id0',
      name: 'name0',
      type: Type::ARTIST,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  available_markets: [
    'available_markets4',
    'available_markets5',
    'available_markets6'
  ],
  disc_number: 104,
  duration_ms: 40,
  explicit: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



