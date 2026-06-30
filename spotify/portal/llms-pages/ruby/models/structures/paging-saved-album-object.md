# Paging Saved Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkQWxidW1PYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PagingSavedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[SavedAlbumObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/saved-album-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_saved_album_object = PagingSavedAlbumObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    SavedAlbumObject.new(
      added_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      album: AlbumObject.new(
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
        tracks: PagingSimplifiedTrackObject.new(
          href: 'href6',
          limit: 142,
          mnext: 'next8',
          offset: 238,
          previous: 'previous2',
          total: 236,
          items: [
            SimplifiedTrackObject.new(
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
                )
              ],
              available_markets: [
                'available_markets2'
              ],
              disc_number: 244,
              duration_ms: 52,
              explicit: false,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            )
          ],
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        copyrights: [
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        external_ids: ExternalIdObject.new(
          isrc: 'isrc8',
          ean: 'ean8',
          upc: 'upc2',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        genres: [
          'genres5',
          'genres6',
          'genres7'
        ],
        label: 'label8',
        popularity: 78,
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



