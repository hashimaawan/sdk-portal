# Paged Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBhZ2VkQWxidW1z

*This model accepts additional fields of type unknown.*


# Interface Name

`PagedAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `albums` | [`PagingSimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/paging-simplified-album-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  PagedAlbums,
  Reason,
  ReleaseDatePrecision,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagedAlbums: PagedAlbums = {
  albums: {
    href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit: 20,
    next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset: 0,
    previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total: 4,
    items: [
      {
        albumType: AlbumType.Compilation,
        totalTracks: 9,
        availableMarkets: [
          'CA',
          'BR',
          'IT'
        ],
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href0',
        id: '2up3OPMp9Tb4dAKM2erWXQ',
        images: [
          {
            url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
            height: 300,
            width: 300,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        name: 'name8',
        releaseDate: '1981-12',
        releaseDatePrecision: ReleaseDatePrecision.Year,
        type: 'album',
        uri: 'spotify:album:2up3OPMp9Tb4dAKM2erWXQ',
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



