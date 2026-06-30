# Resume Point Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VtZVBvaW50T2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ResumePointObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fullyPlayed` | `boolean \| undefined` | Optional | Whether or not the episode has been fully played by the user. |
| `resumePositionMs` | `number \| undefined` | Optional | The user's most recent position in the episode in milliseconds. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ResumePointObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const resumePointObject: ResumePointObject = {
  fullyPlayed: false,
  resumePositionMs: 106,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



