# Search Items

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlNlYXJjaEl0ZW1z

*This model accepts additional fields of type Object.*


# Class Name

`SearchItems`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tracks` | [`PagingTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-track-object.md) | Optional | - |
| `artists` | [`PagingArtistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-artist-object.md) | Optional | - |
| `albums` | [`PagingSimplifiedAlbumObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-simplified-album-object.md) | Optional | - |
| `playlists` | [`PagingPlaylistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-playlist-object.md) | Optional | - |
| `shows` | [`PagingSimplifiedShowObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-simplified-show-object.md) | Optional | - |
| `episodes` | [`PagingSimplifiedEpisodeObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-simplified-episode-object.md) | Optional | - |
| `audiobooks` | [`PagingSimplifiedAudiobookObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/paging-simplified-audiobook-object.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
search_items = SearchItems.new(
  tracks: PagingTrackObject.new(
    href: 'href6',
    limit: 142,
    mnext: 'next8',
    offset: 238,
    previous: 'previous2',
    total: 236,
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
  ),
  artists: PagingArtistObject.new(
    href: 'href2',
    limit: 214,
    mnext: 'next2',
    offset: 54,
    previous: 'previous8',
    total: 52,
    items: [
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
          'genres5',
          'genres6'
        ],
        href: 'href0',
        id: 'id8',
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
          'genres5',
          'genres6'
        ],
        href: 'href0',
        id: 'id8',
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
          'genres5',
          'genres6'
        ],
        href: 'href0',
        id: 'id8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  albums: PagingSimplifiedAlbumObject.new(
    href: 'href0',
    limit: 0,
    mnext: 'next4',
    offset: 96,
    previous: 'previous6',
    total: 94,
    items: [
      SimplifiedAlbumObject.new(
        album_type: AlbumType::ALBUM,
        total_tracks: 196,
        available_markets: [
          'available_markets2'
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
          ),
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
        release_date_precision: ReleaseDatePrecision::MONTH,
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
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  playlists: PagingPlaylistObject.new(
    href: 'href2',
    limit: 68,
    mnext: 'next2',
    offset: 164,
    previous: 'previous8',
    total: 162,
    items: [
      SimplifiedPlaylistObject.new(
        collaborative: false,
        description: 'description2',
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'href0',
        id: 'id8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      SimplifiedPlaylistObject.new(
        collaborative: false,
        description: 'description2',
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'href0',
        id: 'id8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      SimplifiedPlaylistObject.new(
        collaborative: false,
        description: 'description2',
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'href0',
        id: 'id8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  shows: PagingSimplifiedShowObject.new(
    href: 'href0',
    limit: 248,
    mnext: 'next6',
    offset: 88,
    previous: 'previous6',
    total: 86,
    items: [
      ShowBase.new(
        available_markets: [
          'available_markets2'
        ],
        copyrights: [
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        description: 'description2',
        html_description: 'html_description2',
        explicit: false,
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
          ),
          ImageObject.new(
            url: 'url6',
            height: 182,
            width: 222,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        is_externally_hosted: false,
        languages: [
          'languages5'
        ],
        media_type: 'media_type4',
        name: 'name8',
        publisher: 'publisher4',
        type: 'type2',
        uri: 'uri2',
        total_episodes: 166,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ShowBase.new(
        available_markets: [
          'available_markets2'
        ],
        copyrights: [
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        description: 'description2',
        html_description: 'html_description2',
        explicit: false,
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
          ),
          ImageObject.new(
            url: 'url6',
            height: 182,
            width: 222,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        is_externally_hosted: false,
        languages: [
          'languages5'
        ],
        media_type: 'media_type4',
        name: 'name8',
        publisher: 'publisher4',
        type: 'type2',
        uri: 'uri2',
        total_episodes: 166,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ShowBase.new(
        available_markets: [
          'available_markets2'
        ],
        copyrights: [
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        description: 'description2',
        html_description: 'html_description2',
        explicit: false,
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
          ),
          ImageObject.new(
            url: 'url6',
            height: 182,
            width: 222,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        is_externally_hosted: false,
        languages: [
          'languages5'
        ],
        media_type: 'media_type4',
        name: 'name8',
        publisher: 'publisher4',
        type: 'type2',
        uri: 'uri2',
        total_episodes: 166,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



