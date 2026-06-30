# Paging Featured Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ0ZlYXR1cmVkUGxheWxpc3RPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingFeaturedPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `string \| undefined` | Optional | The localized message of a playlist. |
| `playlists` | [`PagingPlaylistObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-playlist-object.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PagingFeaturedPlaylistObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingFeaturedPlaylistObject: PagingFeaturedPlaylistObject = {
  message: 'Popular Playlists',
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



