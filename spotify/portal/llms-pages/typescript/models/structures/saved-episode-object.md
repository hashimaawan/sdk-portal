# Saved Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlNhdmVkRXBpc29kZU9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`SavedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addedAt` | `string \| undefined` | Optional | The date and time the episode was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ. |
| `episode` | [`EpisodeObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/episode-object.md) | Optional | Information about the episode. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ReleaseDatePrecision,
  SavedEpisodeObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const savedEpisodeObject: SavedEpisodeObject = {
  addedAt: '2016-03-13T12:52:32.123Z',
  episode: {
    audioPreviewUrl: 'audio_preview_url8',
    description: 'description2',
    htmlDescription: 'html_description8',
    durationMs: 46,
    explicit: false,
    externalUrls: {
      spotify: 'spotify6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    href: 'href4',
    id: 'id2',
    images: [
      {
        url: 'url6',
        height: 182,
        width: 222,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        url: 'url6',
        height: 182,
        width: 222,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        url: 'url6',
        height: 182,
        width: 222,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    isExternallyHosted: false,
    isPlayable: false,
    languages: [
      'languages9',
      'languages0',
      'languages1'
    ],
    name: 'name2',
    releaseDate: 'release_date0',
    releaseDatePrecision: ReleaseDatePrecision.Year,
    type: 'type8',
    uri: 'uri6',
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
        },
        {
          text: 'text2',
          type: 'type2',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
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
          url: 'url6',
          height: 182,
          width: 222,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          url: 'url6',
          height: 182,
          width: 222,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          url: 'url6',
          height: 182,
          width: 222,
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
      type: 'type4',
      uri: 'uri0',
      totalEpisodes: 198,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    language: 'language4',
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
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



