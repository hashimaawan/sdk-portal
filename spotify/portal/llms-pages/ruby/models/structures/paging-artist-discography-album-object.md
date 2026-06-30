# Paging Artist Discography Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ0FydGlzdERpc2NvZ3JhcGh5QWxidW1PYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PagingArtistDiscographyAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[ArtistDiscographyAlbumObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/artist-discography-album-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_artist_discography_album_object = PagingArtistDiscographyAlbumObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    ArtistDiscographyAlbumObject.new(
      album_type: AlbumType::COMPILATION,
      total_tracks: 9,
      available_markets: [
        'CA',
        'BR',
        'IT'
      ],
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href0',
      id: '2up3OPMp9Tb4dAKM2erWXQ',
      images: [
        ImageObject.new(
          url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
          height: 300,
          width: 300,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      name: 'name8',
      release_date: '1981-12',
      release_date_precision: ReleaseDatePrecision::YEAR,
      type: 'album',
      uri: 'spotify:album:2up3OPMp9Tb4dAKM2erWXQ',
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
      album_group: AlbumGroup::COMPILATION,
      restrictions: AlbumRestrictionObject.new(
        reason: Reason::EXPLICIT,
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



