# Search Items

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlNlYXJjaEl0ZW1z

*This model accepts additional fields of type unknown.*


# Interface Name

`SearchItems`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tracks` | [`PagingTrackObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-track-object.md) | Optional | - |
| `artists` | [`PagingArtistObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-artist-object.md) | Optional | - |
| `albums` | [`PagingSimplifiedAlbumObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-simplified-album-object.md) | Optional | - |
| `playlists` | [`PagingPlaylistObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-playlist-object.md) | Optional | - |
| `shows` | [`PagingSimplifiedShowObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-simplified-show-object.md) | Optional | - |
| `episodes` | [`PagingSimplifiedEpisodeObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-simplified-episode-object.md) | Optional | - |
| `audiobooks` | [`PagingSimplifiedAudiobookObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-simplified-audiobook-object.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  Reason,
  ReleaseDatePrecision,
  SearchItems,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const searchItems: SearchItems = {
  tracks: {
    href: 'href6',
    limit: 142,
    next: 'next8',
    offset: 238,
    previous: 'previous2',
    total: 236,
    items: [
      {
        album: {
          albumType: AlbumType.Single,
          totalTracks: 170,
          availableMarkets: [
            'available_markets2',
            'available_markets3'
          ],
          externalUrls: {
            spotify: 'spotify6',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          href: 'href0',
          id: 'id8',
          images: [
            {
              url: 'url6',
              height: 182,
              width: 222,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            }
          ],
          name: 'name8',
          releaseDate: 'release_date6',
          releaseDatePrecision: ReleaseDatePrecision.Day,
          type: 'type2',
          uri: 'uri2',
          artists: [
            {
              externalUrls: {
                spotify: 'spotify6',
                additionalProperties: {
                  'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
                },
              },
              href: 'href2',
              id: 'id0',
              name: 'name0',
              type: Type.Artist,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            {
              externalUrls: {
                spotify: 'spotify6',
                additionalProperties: {
                  'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
                },
              },
              href: 'href2',
              id: 'id0',
              name: 'name0',
              type: Type.Artist,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            }
          ],
          restrictions: {
            reason: Reason.Explicit,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        artists: [
          {
            externalUrls: {
              spotify: 'spotify6',
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            followers: {
              href: 'href0',
              total: 82,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            genres: [
              'genres7',
              'genres8'
            ],
            href: 'href2',
            id: 'id0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        availableMarkets: [
          'available_markets2'
        ],
        discNumber: 244,
        durationMs: 52,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  artists: {
    href: 'href2',
    limit: 214,
    next: 'next2',
    offset: 54,
    previous: 'previous8',
    total: 52,
    items: [
      {
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        followers: {
          href: 'href0',
          total: 82,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        genres: [
          'genres5',
          'genres6'
        ],
        href: 'href0',
        id: 'id8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        followers: {
          href: 'href0',
          total: 82,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        genres: [
          'genres5',
          'genres6'
        ],
        href: 'href0',
        id: 'id8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        followers: {
          href: 'href0',
          total: 82,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        genres: [
          'genres5',
          'genres6'
        ],
        href: 'href0',
        id: 'id8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  albums: {
    href: 'href0',
    limit: 0,
    next: 'next4',
    offset: 96,
    previous: 'previous6',
    total: 94,
    items: [
      {
        albumType: AlbumType.Album,
        totalTracks: 196,
        availableMarkets: [
          'available_markets2'
        ],
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        images: [
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        name: 'name8',
        releaseDate: 'release_date6',
        releaseDatePrecision: ReleaseDatePrecision.Month,
        type: 'type2',
        uri: 'uri2',
        artists: [
          {
            externalUrls: {
              spotify: 'spotify6',
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            href: 'href2',
            id: 'id0',
            name: 'name0',
            type: Type.Artist,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        restrictions: {
          reason: Reason.Explicit,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  playlists: {
    href: 'href2',
    limit: 68,
    next: 'next2',
    offset: 164,
    previous: 'previous8',
    total: 162,
    items: [
      {
        collaborative: false,
        description: 'description2',
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        collaborative: false,
        description: 'description2',
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        collaborative: false,
        description: 'description2',
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  shows: {
    href: 'href0',
    limit: 248,
    next: 'next6',
    offset: 88,
    previous: 'previous6',
    total: 86,
    items: [
      {
        availableMarkets: [
          'available_markets2'
        ],
        copyrights: [
          {
            text: 'text2',
            type: 'type2',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        description: 'description2',
        htmlDescription: 'html_description2',
        explicit: false,
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        images: [
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        isExternallyHosted: false,
        languages: [
          'languages5'
        ],
        mediaType: 'media_type4',
        name: 'name8',
        publisher: 'publisher4',
        type: 'type2',
        uri: 'uri2',
        totalEpisodes: 166,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        availableMarkets: [
          'available_markets2'
        ],
        copyrights: [
          {
            text: 'text2',
            type: 'type2',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        description: 'description2',
        htmlDescription: 'html_description2',
        explicit: false,
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        images: [
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        isExternallyHosted: false,
        languages: [
          'languages5'
        ],
        mediaType: 'media_type4',
        name: 'name8',
        publisher: 'publisher4',
        type: 'type2',
        uri: 'uri2',
        totalEpisodes: 166,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        availableMarkets: [
          'available_markets2'
        ],
        copyrights: [
          {
            text: 'text2',
            type: 'type2',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        description: 'description2',
        htmlDescription: 'html_description2',
        explicit: false,
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: 'id8',
        images: [
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          {
            url: 'url6',
            height: 182,
            width: 222,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        isExternallyHosted: false,
        languages: [
          'languages5'
        ],
        mediaType: 'media_type4',
        name: 'name8',
        publisher: 'publisher4',
        type: 'type2',
        uri: 'uri2',
        totalEpisodes: 166,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



