# Many Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlBbGJ1bXM

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `albums` | [`AlbumObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/album-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  ManyAlbums,
  Reason,
  ReleaseDatePrecision,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyAlbums: ManyAlbums = {
  albums: [
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
      tracks: {
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
      },
      copyrights: [
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
        'Egg punk',
        'Noise rock'
      ],
      label: 'label8',
      popularity: 66,
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
};
```



