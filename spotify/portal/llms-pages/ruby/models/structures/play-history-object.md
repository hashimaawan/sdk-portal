# Play History Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `track` | [`TrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/track-object.md) | Optional | The track the user listened to. |
| `played_at` | `DateTime` | Optional | The date and time the track was played. |
| `context` | [`ContextObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/context-object.md) | Optional | The context the track was played from. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
play_history_object = PlayHistoryObject.new(
  track: TrackObject.new(
    album: SimplifiedAlbumObject.new(
      album_type: AlbumType::SINGLE,
      total_tracks: 170,
      available_markets: [
        'available_markets2',
        'available_markets3'
      ],
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href0',
      id: 'id8',
      images: [
        ImageObject.new(
          url: 'url6',
          height: 182,
          width: 222,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      name: 'name8',
      release_date: 'release_date6',
      release_date_precision: ReleaseDatePrecision::DAY,
      type: 'type2',
      uri: 'uri2',
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
        )
      ],
      restrictions: AlbumRestrictionObject.new(
        reason: Reason::EXPLICIT,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    artists: [
      ArtistObject.new(
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        followers: FollowersObject.new(
          href: 'href0',
          total: 82,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        genres: [
          'genres7',
          'genres8'
        ],
        href: 'href2',
        id: 'id0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    available_markets: [
      'available_markets8'
    ],
    disc_number: 206,
    duration_ms: 142,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  played_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  context: ContextObject.new(
    type: 'type8',
    href: 'href4',
    external_urls: ExternalUrlObject.new(
      spotify: 'spotify6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    uri: 'uri6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



