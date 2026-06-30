# Saved Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlNhdmVkU2hvd09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`SavedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addedAt` | `string \| undefined` | Optional | The date and time the show was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `show` | [`ShowBase \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/show-base.md) | Optional | Information about the show. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  SavedShowObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const savedShowObject: SavedShowObject = {
  addedAt: '2016-03-13T12:52:32.123Z',
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



