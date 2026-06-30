# Many Episodes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRk1hbnlFcGlzb2Rlcw

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyEpisodes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `episodes` | [`EpisodeObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/episode-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManyEpisodes,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyEpisodes: ManyEpisodes = {
  episodes: [
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
      show: {
        availableMarkets: [
          'available_markets0',
          'available_markets1',
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
        description: 'description4',
        htmlDescription: 'html_description4',
        explicit: false,
        externalUrls: {
          spotify: 'spotify6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        href: 'href8',
        id: 'id6',
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
          'languages7',
          'languages6',
          'languages5'
        ],
        mediaType: 'media_type6',
        name: 'name6',
        publisher: 'publisher6',
        type: 'show',
        uri: 'uri0',
        totalEpisodes: 198,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
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



