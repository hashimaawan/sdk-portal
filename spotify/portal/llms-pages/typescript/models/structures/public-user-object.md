# Public User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlB1YmxpY1VzZXJPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`PublicUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `displayName` | `string \| null \| undefined` | Optional | The name displayed on the user's profile. `null` if not available. |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `followers` | [`FollowersObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint for this user. |
| `id` | `string \| undefined` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `images` | [`ImageObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/image-object.md) | Optional | The user's profile image. |
| `type` | [`Type3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/enumerations/type-3.md) | Optional | The object type. |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PublicUserObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const publicUserObject: PublicUserObject = {
  displayName: 'display_name0',
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
  href: 'href2',
  id: 'id0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



