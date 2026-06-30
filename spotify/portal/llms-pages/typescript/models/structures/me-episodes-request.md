# Me Episodes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRk1lJTI1MjBFcGlzb2RlcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`MeEpisodesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `string[]` | Required | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). <br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  MeEpisodesRequest,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const meEpisodesRequest: MeEpisodesRequest = {
  ids: [
    'ids7'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



