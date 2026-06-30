# Saved Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlNhdmVkVHJhY2tPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`SavedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `DateTime` | Optional | The date and time the track was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `track` | [`TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/track-object.md) | Optional | Information about the track. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
saved_track_object = SavedTrackObject.new(
  added_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
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
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



