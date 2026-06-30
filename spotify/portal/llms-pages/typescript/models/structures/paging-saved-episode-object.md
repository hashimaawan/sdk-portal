# Paging Saved Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkRXBpc29kZU9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingSavedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `number` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| null` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `number` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `string \| null` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `number` | Required | The total number of items available to return. |
| `items` | [`SavedEpisodeObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/saved-episode-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PagingSavedEpisodeObject,
  ReleaseDatePrecision,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingSavedEpisodeObject: PagingSavedEpisodeObject = {
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



