# Me Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRk1lJTI1MjBUcmFja3MlMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type unknown.*


# Interface Name

`MeTracksRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `string[] \| undefined` | Optional | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `["4iV5W9uYEdYUVa79Axb7Rh", "1301WleyT98MSxVHPZCA6M"]`<br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  MeTracksRequest1,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const meTracksRequest1: MeTracksRequest1 = {
  ids: [
    'ids3',
    'ids4'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



