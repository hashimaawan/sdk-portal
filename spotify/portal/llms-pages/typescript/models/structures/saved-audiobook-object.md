# Saved Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlNhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`SavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addedAt` | `string \| undefined` | Optional | The date and time the audiobook was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `audiobook` | [`AudiobookObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/audiobook-object.md) | Optional | Information about the audiobook. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ReleaseDatePrecision,
  SavedAudiobookObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const savedAudiobookObject: SavedAudiobookObject = {
  addedAt: '2016-03-13T12:52:32.123Z',
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
      },
      {
        name: 'name0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    publisher: 'publisher4',
    type: 'type2',
    uri: 'uri2',
    totalChapters: 186,
    chapters: {
      href: 'href4',
      limit: 230,
      next: 'next0',
      offset: 122,
      previous: 'previous0',
      total: 136,
      items: [
        {
          audioPreviewUrl: 'audio_preview_url4',
          chapterNumber: 164,
          description: 'description2',
          htmlDescription: 'html_description2',
          durationMs: 52,
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
          isPlayable: false,
          languages: [
            'languages5'
          ],
          name: 'name8',
          releaseDate: 'release_date6',
          releaseDatePrecision: ReleaseDatePrecision.Month,
          type: 'type2',
          uri: 'uri2',
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
    edition: 'edition8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



