# Explicit Content Settings Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkV4cGxpY2l0Q29udGVudFNldHRpbmdzT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ExplicitContentSettingsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filterEnabled` | `boolean \| undefined` | Optional | When `true`, indicates that explicit content should not be played. |
| `filterLocked` | `boolean \| undefined` | Optional | When `true`, indicates that the explicit content setting is locked and can't be changed by the user. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ExplicitContentSettingsObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const explicitContentSettingsObject: ExplicitContentSettingsObject = {
  filterEnabled: false,
  filterLocked: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



