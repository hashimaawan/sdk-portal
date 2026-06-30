# Cursor Paging Simplified Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1NpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`CursorPagingSimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `number \| undefined` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| undefined` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `number \| undefined` | Optional | The total number of items available to return. |
| `items` | [`ArtistObject[] \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/artist-object.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CursorPagingSimplifiedArtistObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const cursorPagingSimplifiedArtistObject: CursorPagingSimplifiedArtistObject = {
  href: 'href2',
  limit: 24,
  next: 'next2',
  cursors: {
    after: 'after8',
    before: 'before6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  total: 118,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



