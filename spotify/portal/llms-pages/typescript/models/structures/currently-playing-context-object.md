# Currently Playing Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device` | [`DeviceObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/device-object.md) | Optional | The device that is currently active. |
| `repeatState` | `string \| undefined` | Optional | off, track, context |
| `shuffleState` | `boolean \| undefined` | Optional | If shuffle is on or off. |
| `context` | [`ContextObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `timestamp` | `bigint \| undefined` | Optional | Unix Millisecond Timestamp when data was fetched. |
| `progressMs` | `number \| undefined` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `isPlaying` | `boolean \| undefined` | Optional | If something is currently playing, return `true`. |
| `item` | [`CurrentlyPlayingContextObjectItem \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/oneof-anyof-definitions/currently-playing-context-object-item.md) | Optional | This is a container for one-of cases. |
| `currentlyPlayingType` | `string \| undefined` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `actions` | [`DisallowsObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CurrentlyPlayingContextObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const currentlyPlayingContextObject: CurrentlyPlayingContextObject = {
  device: {
    id: 'id6',
    isActive: false,
    isPrivateSession: false,
    isRestricted: false,
    name: 'name6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  repeatState: 'repeat_state8',
  shuffleState: false,
  context: {
    type: 'type8',
    href: 'href4',
    externalUrls: {
      spotify: 'spotify6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    uri: 'uri6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  timestamp: BigInt(48),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



