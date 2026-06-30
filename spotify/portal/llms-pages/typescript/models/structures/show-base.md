# Show Base

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlNob3dCYXNl

*This model accepts additional fields of type unknown.*


# Interface Name

`ShowBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `availableMarkets` | `string[]` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`CopyrightObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `description` | `string` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `htmlDescription` | `string` | Required | A description of the show. This field may contain HTML tags. |
| `explicit` | `boolean` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `externalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the show. |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `images` | [`ImageObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `isExternallyHosted` | `boolean` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `languages` | `string[]` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `mediaType` | `string` | Required | The media type of the show. |
| `name` | `string` | Required | The name of the episode. |
| `publisher` | `string` | Required | The publisher of the show. |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'show'` |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `totalEpisodes` | `number` | Required | The total number of episodes in the show. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ShowBase,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const showBase: ShowBase = {
  availableMarkets: [
    'available_markets2',
    'available_markets3'
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
  isExternallyHosted: false,
  languages: [
    'languages3',
    'languages4',
    'languages5'
  ],
  mediaType: 'media_type4',
  name: 'name8',
  publisher: 'publisher4',
  type: 'show',
  uri: 'uri2',
  totalEpisodes: 144,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



