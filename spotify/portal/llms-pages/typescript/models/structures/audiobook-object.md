# Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkF1ZGlvYm9va09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`AudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authors` | [`AuthorObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `availableMarkets` | `string[]` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`CopyrightObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `description` | `string` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `htmlDescription` | `string` | Required | A description of the audiobook. This field may contain HTML tags. |
| `edition` | `string \| undefined` | Optional | The edition of the audiobook. |
| `explicit` | `boolean` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `externalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `images` | [`ImageObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `languages` | `string[]` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `mediaType` | `string` | Required | The media type of the audiobook. |
| `name` | `string` | Required | The name of the audiobook. |
| `narrators` | [`NarratorObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `publisher` | `string` | Required | The publisher of the audiobook. |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'audiobook'` |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `totalChapters` | `number` | Required | The number of chapters in this audiobook. |
| `chapters` | [`PagingSimplifiedChapterObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/paging-simplified-chapter-object.md) | Required | The chapters of the audiobook. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AudiobookObject,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const audiobookObject: AudiobookObject = {
  authors: [
    {
      name: 'name0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  availableMarkets: [
    'available_markets4',
    'available_markets5'
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
  description: 'description0',
  htmlDescription: 'html_description0',
  explicit: false,
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  href: 'href2',
  id: 'id0',
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
    'languages1',
    'languages2',
    'languages3'
  ],
  mediaType: 'media_type2',
  name: 'name0',
  narrators: [
    {
      name: 'name0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  publisher: 'publisher2',
  type: 'audiobook',
  uri: 'uri4',
  totalChapters: 72,
  chapters: {
    href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit: 20,
    next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset: 0,
    previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total: 4,
    items: [
      {
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
        availableMarkets: [
          'available_markets2'
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
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  edition: 'Unabridged',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



