# Paging Simplified Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRUcmFja09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingSimplifiedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `number` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| null` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `number` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `string \| null` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `number` | Required | The total number of items available to return. |
| `items` | [`SimplifiedTrackObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/simplified-track-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PagingSimplifiedTrackObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingSimplifiedTrackObject: PagingSimplifiedTrackObject = {
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
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
};
```



