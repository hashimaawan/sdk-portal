# Playlist User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBsYXlsaXN0VXNlck9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`PlaylistUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `followers` | [`FollowersObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint for this user. |
| `id` | `string \| undefined` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `type` | [`Type3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/enumerations/type-3.md) | Optional | The object type. |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PlaylistUserObject,
  Type3,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const playlistUserObject: PlaylistUserObject = {
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  followers: {
    href: 'href0',
    total: 82,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  href: 'href0',
  id: 'id8',
  type: Type3.User,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



