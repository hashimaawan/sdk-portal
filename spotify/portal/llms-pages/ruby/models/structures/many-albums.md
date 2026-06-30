# Many Albums

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRk1hbnlBbGJ1bXM

*This model accepts additional fields of type Object.*


# Class Name

`ManyAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `albums` | [`Array[AlbumObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/album-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
many_albums = ManyAlbums.new(
  albums: [
    AlbumObject.new(
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
      tracks: PagingSimplifiedTrackObject.new(
        href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
        limit: 20,
        mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
        offset: 0,
        previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
        total: 4,
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
        'Egg punk',
        'Noise rock'
      ],
      label: 'label8',
      popularity: 66,
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



