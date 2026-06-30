# Many Audiobooks

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlBdWRpb2Jvb2tz

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyAudiobooks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audiobooks` | [`AudiobookObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/audiobook-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManyAudiobooks,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyAudiobooks: ManyAudiobooks = {
  audiobooks: [
    {
      authors: [
        {
          name: 'name0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      availableMarkets: [
        'available_markets8'
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
      htmlDescription: 'html_description6',
      explicit: false,
      externalUrls: {
        spotify: 'spotify6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      href: 'href6',
      id: 'id4',
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
        'languages1'
      ],
      mediaType: 'media_type8',
      name: 'name4',
      narrators: [
        {
          name: 'name0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      publisher: 'publisher8',
      type: 'audiobook',
      uri: 'uri8',
      totalChapters: 186,
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



