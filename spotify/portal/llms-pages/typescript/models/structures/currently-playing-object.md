# Currently Playing Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`CurrentlyPlayingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | [`ContextObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `timestamp` | `bigint \| undefined` | Optional | Unix Millisecond Timestamp when data was fetched |
| `progressMs` | `number \| undefined` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `isPlaying` | `boolean \| undefined` | Optional | If something is currently playing, return `true`. |
| `item` | [`CurrentlyPlayingObjectItem \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/oneof-anyof-definitions/currently-playing-object-item.md) | Optional | This is a container for one-of cases. |
| `currentlyPlayingType` | `string \| undefined` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `actions` | [`DisallowsObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  CurrentlyPlayingObject,
  Reason,
  ReleaseDatePrecision,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const currentlyPlayingObject: CurrentlyPlayingObject = {
  context: {
    type: 'type8',
    href: 'href4',
    externalUrls: {
      spotify: 'spotify6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    uri: 'uri6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  timestamp: BigInt(254),
  progressMs: 226,
  isPlaying: false,
  item: {
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



