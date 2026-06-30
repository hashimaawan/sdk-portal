# Currently Playing Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`CurrentlyPlayingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `timestamp` | `Integer` | Optional | Unix Millisecond Timestamp when data was fetched |
| `progress_ms` | `Integer` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `is_playing` | `TrueClass \| FalseClass` | Optional | If something is currently playing, return `true`. |
| `item` | [TrackObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/track-object.md) \| [EpisodeObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/episode-object.md) \| nil | Optional | This is a container for one-of cases. |
| `currently_playing_type` | `String` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
currently_playing_object = CurrentlyPlayingObject.new(
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
  timestamp: 226,
  progress_ms: 198,
  is_playing: false,
  item: TrackObject.new(
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
      ),
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
      'available_markets6',
      'available_markets7'
    ],
    disc_number: 30,
    duration_ms: 222,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



