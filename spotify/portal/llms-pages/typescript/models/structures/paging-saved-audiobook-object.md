# Paging Saved Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingSavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `number` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| null` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `number` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `string \| null` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `number` | Required | The total number of items available to return. |
| `items` | [`SavedAudiobookObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/saved-audiobook-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PagingSavedAudiobookObject,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingSavedAudiobookObject: PagingSavedAudiobookObject = {
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



