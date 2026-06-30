# Playlist Track Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PlaylistTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `DateTime` | Optional | The date and time the track or episode was added. _**Note**: some very old playlists may return `null` in this field._ |
| `added_by` | [`PlaylistUserObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/playlist-user-object.md) | Optional | The Spotify user who added the track or episode. _**Note**: some very old playlists may return `null` in this field._ |
| `is_local` | `TrueClass \| FalseClass` | Optional | Whether this track or episode is a [local file](/documentation/web-api/concepts/playlists/#local-files) or not. |
| `track` | [TrackObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/track-object.md) \| [EpisodeObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/episode-object.md) \| nil | Optional | This is a container for one-of cases. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
playlist_track_object = PlaylistTrackObject.new(
  added_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  added_by: PlaylistUserObject.new(
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
    href: 'href6',
    id: 'id4',
    type: Type3::USER,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  is_local: false,
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



