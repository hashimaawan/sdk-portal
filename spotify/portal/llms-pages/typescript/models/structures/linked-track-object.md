# Linked Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkxpbmtlZFRyYWNrT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`LinkedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known external URLs for this track. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the track. |
| `id` | `string \| undefined` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `type` | `string \| undefined` | Optional | The object type: "track". |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  LinkedTrackObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const linkedTrackObject: LinkedTrackObject = {
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  href: 'href0',
  id: 'id8',
  type: 'type2',
  uri: 'uri2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



