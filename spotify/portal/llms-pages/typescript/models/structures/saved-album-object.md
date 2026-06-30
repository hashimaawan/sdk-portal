# Saved Album Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlNhdmVkQWxidW1PYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`SavedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addedAt` | `string \| undefined` | Optional | The date and time the album was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `album` | [`AlbumObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/album-object.md) | Optional | Information about the album. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  Reason,
  ReleaseDatePrecision,
  SavedAlbumObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const savedAlbumObject: SavedAlbumObject = {
  addedAt: '2016-03-13T12:52:32.123Z',
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
    tracks: {
      href: 'href6',
      limit: 142,
      next: 'next8',
      offset: 238,
      previous: 'previous2',
      total: 236,
      items: [
        {
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
          availableMarkets: [
            'available_markets2'
          ],
          discNumber: 244,
          durationMs: 52,
          explicit: false,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    copyrights: [
      {
        text: 'text2',
        type: 'type2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        text: 'text2',
        type: 'type2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    externalIds: {
      isrc: 'isrc8',
      ean: 'ean8',
      upc: 'upc2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    genres: [
      'genres5',
      'genres6',
      'genres7'
    ],
    label: 'label8',
    popularity: 78,
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



