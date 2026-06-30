# Saved Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlNhdmVkVHJhY2tPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`SavedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addedAt` | `string \| undefined` | Optional | The date and time the track was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `track` | [`TrackObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/track-object.md) | Optional | Information about the track. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  Reason,
  ReleaseDatePrecision,
  SavedTrackObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const savedTrackObject: SavedTrackObject = {
  addedAt: '2016-03-13T12:52:32.123Z',
  track: {
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
      'available_markets8'
    ],
    discNumber: 206,
    durationMs: 142,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



