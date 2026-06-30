# Disallows Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkRpc2FsbG93c09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`DisallowsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `interruptingPlayback` | `boolean \| undefined` | Optional | Interrupting playback. Optional field. |
| `pausing` | `boolean \| undefined` | Optional | Pausing. Optional field. |
| `resuming` | `boolean \| undefined` | Optional | Resuming. Optional field. |
| `seeking` | `boolean \| undefined` | Optional | Seeking playback location. Optional field. |
| `skippingNext` | `boolean \| undefined` | Optional | Skipping to the next context. Optional field. |
| `skippingPrev` | `boolean \| undefined` | Optional | Skipping to the previous context. Optional field. |
| `togglingRepeatContext` | `boolean \| undefined` | Optional | Toggling repeat context flag. Optional field. |
| `togglingShuffle` | `boolean \| undefined` | Optional | Toggling shuffle flag. Optional field. |
| `togglingRepeatTrack` | `boolean \| undefined` | Optional | Toggling repeat track flag. Optional field. |
| `transferringPlayback` | `boolean \| undefined` | Optional | Transfering playback between devices. Optional field. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  DisallowsObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const disallowsObject: DisallowsObject = {
  interruptingPlayback: false,
  pausing: false,
  resuming: false,
  seeking: false,
  skippingNext: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



