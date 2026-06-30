# Me following Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk1lJTI1MjBGb2xsb3dpbmclMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type unknown.*


# Interface Name

`MeFollowingRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `string[] \| undefined` | Optional | A JSON array of the artist or user [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `{ids:["74ASZWbe4lXaubB36ztrGX", "08td7MxkoHQkXnWAYD8d6Q"]}`. A maximum of 50 IDs can be sent in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  MeFollowingRequest1,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const meFollowingRequest1: MeFollowingRequest1 = {
  ids: [
    'ids5',
    'ids6'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



