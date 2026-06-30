# External Url Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkV4dGVybmFsVXJsT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ExternalUrlObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `spotify` | `string \| undefined` | Optional | The [Spotify URL](/documentation/web-api/concepts/spotify-uris-ids) for the object. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ExternalUrlObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const externalUrlObject: ExternalUrlObject = {
  spotify: 'spotify0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



