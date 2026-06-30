# Track 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlRyYWNrMQ

*This model accepts additional fields of type unknown.*


# Interface Name

`Track1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uri` | `string \| undefined` | Optional | Spotify URI |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  Track1,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const track1: Track1 = {
  uri: 'uri0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



