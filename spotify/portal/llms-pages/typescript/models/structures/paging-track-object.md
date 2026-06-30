# Paging Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ1RyYWNrT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `number` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| null` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `number` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `string \| null` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `number` | Required | The total number of items available to return. |
| `items` | [`TrackObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/track-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  PagingTrackObject,
  Reason,
  ReleaseDatePrecision,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingTrackObject: PagingTrackObject = {
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
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
};
```



