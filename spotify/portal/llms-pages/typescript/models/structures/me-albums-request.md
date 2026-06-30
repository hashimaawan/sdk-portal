# Me Albums Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk1lJTI1MjBBbGJ1bXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`MeAlbumsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `string[] \| undefined` | Optional | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `["4iV5W9uYEdYUVa79Axb7Rh", "1301WleyT98MSxVHPZCA6M"]`<br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  MeAlbumsRequest,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const meAlbumsRequest: MeAlbumsRequest = {
  ids: [
    'ids9'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



