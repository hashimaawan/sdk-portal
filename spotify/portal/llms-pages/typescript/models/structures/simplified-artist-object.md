# Simplified Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`SimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `id` | `string \| undefined` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `name` | `string \| undefined` | Optional | The name of the artist. |
| `type` | [`Type \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/enumerations/type.md) | Optional | The object type. |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  SimplifiedArtistObject,
  Type,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const simplifiedArtistObject: SimplifiedArtistObject = {
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  href: 'href6',
  id: 'id4',
  name: 'name4',
  type: Type.Artist,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



