# Queue Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXVlT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`QueueObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currentlyPlaying` | [`QueueObjectCurrentlyPlaying \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/oneof-anyof-definitions/queue-object-currently-playing.md) | Optional | This is a container for one-of cases. |
| `queue` | [`QueueObjectQueue[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/oneof-anyof-definitions/queue-object-queue.md) | Optional | This is Array of a container for one-of cases. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  QueueObject,
  Reason,
  ReleaseDatePrecision,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const queueObject: QueueObject = {
  currentlyPlaying: {
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
      'available_markets6',
      'available_markets7'
    ],
    discNumber: 30,
    durationMs: 222,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  queue: [
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
        'available_markets6',
        'available_markets7'
      ],
      discNumber: 30,
      durationMs: 222,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
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
        'available_markets6',
        'available_markets7'
      ],
      discNumber: 30,
      durationMs: 222,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
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
        'available_markets6',
        'available_markets7'
      ],
      discNumber: 30,
      durationMs: 222,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



