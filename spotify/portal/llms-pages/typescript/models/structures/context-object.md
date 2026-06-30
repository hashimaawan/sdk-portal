# Context Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkNvbnRleHRPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `string \| undefined` | Optional | The object type, e.g. "artist", "playlist", "album", "show". |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the track. |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | External URLs for this context. |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the context. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ContextObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const contextObject: ContextObject = {
  type: 'type6',
  href: 'href6',
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  uri: 'uri8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



