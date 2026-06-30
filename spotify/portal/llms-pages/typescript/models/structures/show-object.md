# Show Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlNob3dPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `availableMarkets` | `string[]` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`CopyrightObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `description` | `string` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `htmlDescription` | `string` | Required | A description of the show. This field may contain HTML tags. |
| `explicit` | `boolean` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `externalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the show. |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `images` | [`ImageObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `isExternallyHosted` | `boolean` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `languages` | `string[]` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `mediaType` | `string` | Required | The media type of the show. |
| `name` | `string` | Required | The name of the episode. |
| `publisher` | `string` | Required | The publisher of the show. |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'show'` |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `totalEpisodes` | `number` | Required | The total number of episodes in the show. |
| `episodes` | [`PagingSimplifiedEpisodeObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/paging-simplified-episode-object.md) | Required | The episodes of the show. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ReleaseDatePrecision,
  ShowObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const showObject: ShowObject = {
  availableMarkets: [
    'available_markets2'
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
  description: 'description8',
  htmlDescription: 'html_description8',
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
    'languages5'
  ],
  mediaType: 'media_type6',
  name: 'name8',
  publisher: 'publisher6',
  type: 'show',
  uri: 'uri2',
  totalEpisodes: 230,
  episodes: {
    href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit: 20,
    next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset: 0,
    previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total: 4,
    items: [
      {
        audioPreviewUrl: 'https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
        description: 'A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n',
        htmlDescription: '<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n',
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
        isExternallyHosted: false,
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
        language: 'en',
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



