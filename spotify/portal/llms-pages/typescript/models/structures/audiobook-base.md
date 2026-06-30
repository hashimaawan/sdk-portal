# Audiobook Base

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkF1ZGlvYm9va0Jhc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`AudiobookBase`


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
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AudiobookBase,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const audiobookBase: AudiobookBase = {
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
    'available_markets5',
    'available_markets6'
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
    'languages7',
    'languages8',
    'languages9'
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
  totalChapters: 120,
  edition: 'Unabridged',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



