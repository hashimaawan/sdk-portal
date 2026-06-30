# Simplified Track Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRUcmFja09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`SimplifiedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`SimplifiedArtistObject[] \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/simplified-artist-object.md) | Optional | The artists who performed the track. Each artist object includes a link in `href` to more detailed information about the artist. |
| `availableMarkets` | `string[] \| undefined` | Optional | A list of the countries in which the track can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `discNumber` | `number \| undefined` | Optional | The disc number (usually `1` unless the album consists of more than one disc). |
| `durationMs` | `number \| undefined` | Optional | The track length in milliseconds. |
| `explicit` | `boolean \| undefined` | Optional | Whether or not the track has explicit lyrics ( `true` = yes it does; `false` = no it does not OR unknown). |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | External URLs for this track. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the track. |
| `id` | `string \| undefined` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `isPlayable` | `boolean \| undefined` | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking/) is applied. If `true`, the track is playable in the given market. Otherwise `false`. |
| `linkedFrom` | [`LinkedTrackObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/linked-track-object.md) | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking/) is applied and is only part of the response if the track linking, in fact, exists. The requested track has been replaced with a different track. The track in the `linked_from` object contains information about the originally requested track. |
| `restrictions` | [`TrackRestrictionObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/track-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `name` | `string \| undefined` | Optional | The name of the track. |
| `previewUrl` | `string \| null \| undefined` | Optional | A URL to a 30 second preview (MP3 format) of the track. |
| `trackNumber` | `number \| undefined` | Optional | The number of the track. If an album has several discs, the track number is the number on the specified disc. |
| `type` | `string \| undefined` | Optional | The object type: "track". |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `isLocal` | `boolean \| undefined` | Optional | Whether or not the track is from a local file. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  SimplifiedTrackObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const simplifiedTrackObject: SimplifiedTrackObject = {
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
  availableMarkets: [
    'available_markets0',
    'available_markets1',
    'available_markets2'
  ],
  discNumber: 180,
  durationMs: 244,
  explicit: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



