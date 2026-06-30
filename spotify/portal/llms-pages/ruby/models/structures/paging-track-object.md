# Paging Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ1RyYWNrT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PagingTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[TrackObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/track-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_track_object = PagingTrackObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    TrackObject.new(
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
        'available_markets2'
      ],
      disc_number: 244,
      duration_ms: 52,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



