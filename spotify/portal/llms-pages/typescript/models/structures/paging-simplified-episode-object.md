# Paging Simplified Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRFcGlzb2RlT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingSimplifiedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `number` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| null` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `number` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `string \| null` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `number` | Required | The total number of items available to return. |
| `items` | [`EpisodeBase[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/episode-base.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PagingSimplifiedEpisodeObject,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingSimplifiedEpisodeObject: PagingSimplifiedEpisodeObject = {
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
};
```



