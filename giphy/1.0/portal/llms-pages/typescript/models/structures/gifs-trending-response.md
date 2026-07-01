# Gifs Trending Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdpZnMlMjUyMFRyZW5kaW5nJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GifsTrendingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Gif[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `pagination` | [`Pagination \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GifsTrendingResponse } from 'giphy-apilib';

const gifsTrendingResponse: GifsTrendingResponse = {
  data: [
    {
      bitlyUrl: 'bitly_url0',
      contentUrl: 'content_url4',
      createDatetime: '2016-03-13T12:52:32.123Z',
      embdedUrl: 'embded_url8',
      featuredTags: [
        'featured_tags0'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  meta: {
    msg: 'msg8',
    responseId: 'response_id0',
    status: 98,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  pagination: {
    count: 192,
    offset: 240,
    totalCount: 100,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



