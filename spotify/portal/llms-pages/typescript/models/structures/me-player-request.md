# Me Player Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`MePlayerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deviceIds` | `string[]` | Required | A JSON array containing the ID of the device on which playback should be started/transferred.<br/>For example:`{device_ids:["74ASZWbe4lXaubB36ztrGX"]}`<br/>_**Note**: Although an array is accepted, only a single device_id is currently supported. Supplying more than one will return `400 Bad Request`_ |
| `play` | `boolean \| undefined` | Optional | **true**: ensure playback happens on new device.<br/>**false** or not provided: keep the current playback state. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  MePlayerRequest,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const mePlayerRequest: MePlayerRequest = {
  deviceIds: [
    '74ASZWbe4lXaubB36ztrGX'
  ],
  play: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



