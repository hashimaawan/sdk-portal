# Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkFydGlzdE9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`ArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `followers` | [`FollowersObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/followers-object.md) | Optional | Information about the followers of the artist. |
| `genres` | `string[] \| undefined` | Optional | A list of the genres the artist is associated with. If not yet classified, the array is empty. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `id` | `string \| undefined` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `images` | [`ImageObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/image-object.md) | Optional | Images of the artist in various sizes, widest first. |
| `name` | `string \| undefined` | Optional | The name of the artist. |
| `popularity` | `number \| undefined` | Optional | The popularity of the artist. The value will be between 0 and 100, with 100 being the most popular. The artist's popularity is calculated from the popularity of all the artist's tracks. |
| `type` | [`Type \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/enumerations/type.md) | Optional | The object type. |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ArtistObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const artistObject: ArtistObject = {
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
  genres: [
    'Prog rock',
    'Grunge'
  ],
  href: 'href8',
  id: 'id6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



