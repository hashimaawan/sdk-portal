# Cursor Paged Artists

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkN1cnNvclBhZ2VkQXJ0aXN0cw

*This model accepts additional fields of type unknown.*


# Interface Name

`CursorPagedArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`CursorPagingSimplifiedArtistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/cursor-paging-simplified-artist-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CursorPagedArtists,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const cursorPagedArtists: CursorPagedArtists = {
  artists: {
    href: 'href2',
    limit: 214,
    next: 'next2',
    cursors: {
      after: 'after8',
      before: 'before6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    total: 52,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



