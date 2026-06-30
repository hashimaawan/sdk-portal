# Simplified Album Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBbGJ1bU9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`SimplifiedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `albumType` | [`AlbumType`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/enumerations/album-type.md) | Required | The type of the album. |
| `totalTracks` | `number` | Required | The number of tracks in the album. |
| `availableMarkets` | `string[]` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ |
| `externalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Required | Known external URLs for this album. |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the album. |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `images` | [`ImageObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. |
| `name` | `string` | Required | The name of the album. In case of an album takedown, the value may be an empty string. |
| `releaseDate` | `string` | Required | The date the album was first released. |
| `releaseDatePrecision` | [`ReleaseDatePrecision`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `restrictions` | [`AlbumRestrictionObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'album'` |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `artists` | [`SimplifiedArtistObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  Reason,
  ReleaseDatePrecision,
  SimplifiedAlbumObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const simplifiedAlbumObject: SimplifiedAlbumObject = {
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
  href: 'href4',
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
  name: 'name2',
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
};
```



