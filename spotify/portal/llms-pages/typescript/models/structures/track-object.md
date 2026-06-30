# Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlRyYWNrT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`TrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `album` | [`SimplifiedAlbumObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/simplified-album-object.md) | Optional | The album on which the track appears. The album object includes a link in `href` to full information about the album. |
| `artists` | [`ArtistObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/artist-object.md) | Optional | The artists who performed the track. Each artist object includes a link in `href` to more detailed information about the artist. |
| `availableMarkets` | `string[] \| undefined` | Optional | A list of the countries in which the track can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `discNumber` | `number \| undefined` | Optional | The disc number (usually `1` unless the album consists of more than one disc). |
| `durationMs` | `number \| undefined` | Optional | The track length in milliseconds. |
| `explicit` | `boolean \| undefined` | Optional | Whether or not the track has explicit lyrics ( `true` = yes it does; `false` = no it does not OR unknown). |
| `externalIds` | [`ExternalIdObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/external-id-object.md) | Optional | Known external IDs for the track. |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known external URLs for this track. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the track. |
| `id` | `string \| undefined` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `isPlayable` | `boolean \| undefined` | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking) is applied. If `true`, the track is playable in the given market. Otherwise `false`. |
| `linkedFrom` | [`LinkedTrackObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/linked-track-object.md) | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking) is applied, and the requested track has been replaced with different track. The track in the `linked_from` object contains information about the originally requested track. |
| `restrictions` | [`TrackRestrictionObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/track-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `name` | `string \| undefined` | Optional | The name of the track. |
| `popularity` | `number \| undefined` | Optional | The popularity of the track. The value will be between 0 and 100, with 100 being the most popular.<br/>The popularity of a track is a value between 0 and 100, with 100 being the most popular. The popularity is calculated by algorithm and is based, in the most part, on the total number of plays the track has had and how recent those plays are.<br/>Generally speaking, songs that are being played a lot now will have a higher popularity than songs that were played a lot in the past. Duplicate tracks (e.g. the same track from a single and an album) are rated independently. Artist and album popularity is derived mathematically from track popularity. _**Note**: the popularity value may lag actual popularity by a few days: the value is not updated in real time._ |
| `previewUrl` | `string \| null \| undefined` | Optional | A link to a 30 second preview (MP3 format) of the track. Can be `null` |
| `trackNumber` | `number \| undefined` | Optional | The number of the track. If an album has several discs, the track number is the number on the specified disc. |
| `type` | [`Type2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/enumerations/type-2.md) | Optional | The object type: "track". |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `isLocal` | `boolean \| undefined` | Optional | Whether or not the track is from a local file. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AlbumType,
  Reason,
  ReleaseDatePrecision,
  TrackObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const trackObject: TrackObject = {
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
    },
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
    'available_markets2',
    'available_markets3',
    'available_markets4'
  ],
  discNumber: 182,
  durationMs: 246,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



