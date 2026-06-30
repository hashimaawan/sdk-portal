# Many Simplified Shows

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlTaW1wbGlmaWVkU2hvd3M

*This model accepts additional fields of type unknown.*


# Interface Name

`ManySimplifiedShows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `shows` | [`ShowBase[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/show-base.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManySimplifiedShows,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manySimplifiedShows: ManySimplifiedShows = {
  shows: [
    {
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
        'languages5'
      ],
      mediaType: 'media_type4',
      name: 'name8',
      publisher: 'publisher4',
      type: 'show',
      uri: 'uri2',
      totalEpisodes: 196,
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



