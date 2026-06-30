# Many Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlBcnRpc3Rz

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`ArtistObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/artist-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManyArtists,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyArtists: ManyArtists = {
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
        'Prog rock',
        'Grunge'
      ],
      href: 'href2',
      id: 'id0',
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



