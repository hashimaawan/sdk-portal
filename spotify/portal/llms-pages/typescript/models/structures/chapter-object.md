# Chapter Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkNoYXB0ZXJPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ChapterObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audioPreviewUrl` | `string \| null` | Required | A URL to a 30 second preview (MP3 format) of the chapter. `null` if not available. |
| `availableMarkets` | `string[] \| undefined` | Optional | A list of the countries in which the chapter can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `chapterNumber` | `number` | Required | The number of the chapter |
| `description` | `string` | Required | A description of the chapter. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `htmlDescription` | `string` | Required | A description of the chapter. This field may contain HTML tags. |
| `durationMs` | `number` | Required | The chapter length in milliseconds. |
| `explicit` | `boolean` | Required | Whether or not the chapter has explicit content (true = yes it does; false = no it does not OR unknown). |
| `externalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Required | External URLs for this chapter. |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the chapter. |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the chapter. |
| `images` | [`ImageObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/image-object.md) | Required | The cover art for the chapter in various sizes, widest first. |
| `isPlayable` | `boolean` | Required | True if the chapter is playable in the given market. Otherwise false. |
| `languages` | `string[]` | Required | A list of the languages used in the chapter, identified by their [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639) code. |
| `name` | `string` | Required | The name of the chapter. |
| `releaseDate` | `string` | Required | The date the chapter was first released, for example `"1981-12-15"`. Depending on the precision, it might be shown as `"1981"` or `"1981-12"`. |
| `releaseDatePrecision` | [`ReleaseDatePrecision`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `resumePoint` | [`ResumePointObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/resume-point-object.md) | Optional | The user's most recent position in the chapter. Set if the supplied access token is a user token and has the scope 'user-read-playback-position'. |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'episode'` |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the chapter. |
| `restrictions` | [`ChapterRestrictionObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/chapter-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `audiobook` | [`AudiobookBase`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/audiobook-base.md) | Required | The audiobook for which the chapter belongs. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ChapterObject,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const chapterObject: ChapterObject = {
  audioPreviewUrl: 'https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
  chapterNumber: 1,
  description: 'We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.\n',
  htmlDescription: '<p>We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.</p>\n',
  durationMs: 1686230,
  explicit: false,
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  href: 'https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ',
  id: '5Xt5DXGzch68nYYamXrNxZ',
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
  isPlayable: false,
  languages: [
    'fr',
    'en'
  ],
  name: 'Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n',
  releaseDate: '1981-12-15',
  releaseDatePrecision: ReleaseDatePrecision.Day,
  type: 'episode',
  uri: 'spotify:episode:0zLhl3WsOCQHbe1BPTiHgr',
  audiobook: {
    authors: [
      {
        name: 'name0',
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
    copyrights: [
      {
        text: 'text2',
        type: 'type2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    description: 'description2',
    htmlDescription: 'html_description2',
    explicit: false,
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
        url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
        height: 300,
        width: 300,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    languages: [
      'languages3',
      'languages4'
    ],
    mediaType: 'media_type4',
    name: 'name8',
    narrators: [
      {
        name: 'name0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    publisher: 'publisher4',
    type: 'audiobook',
    uri: 'uri2',
    totalChapters: 186,
    edition: 'Unabridged',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  availableMarkets: [
    'available_markets4'
  ],
  resumePoint: {
    fullyPlayed: false,
    resumePositionMs: 254,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  restrictions: {
    reason: 'reason0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



