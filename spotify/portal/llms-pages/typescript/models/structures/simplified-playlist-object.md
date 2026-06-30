# Simplified Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRQbGF5bGlzdE9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`SimplifiedPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `collaborative` | `boolean \| undefined` | Optional | `true` if the owner allows other users to modify the playlist. |
| `description` | `string \| undefined` | Optional | The playlist description. _Only returned for modified, verified playlists, otherwise_ `null`. |
| `externalUrls` | [`ExternalUrlObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/external-url-object.md) | Optional | Known external URLs for this playlist. |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint providing full details of the playlist. |
| `id` | `string \| undefined` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the playlist. |
| `images` | [`ImageObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/image-object.md) | Optional | Images for the playlist. The array may be empty or contain up to three images. The images are returned by size in descending order. See [Working with Playlists](/documentation/web-api/concepts/playlists). _**Note**: If returned, the source URL for the image (`url`) is temporary and will expire in less than a day._ |
| `name` | `string \| undefined` | Optional | The name of the playlist. |
| `owner` | [`PlaylistOwnerObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/playlist-owner-object.md) | Optional | The user who owns the playlist |
| `mPublic` | `boolean \| undefined` | Optional | The playlist's public/private status: `true` the playlist is public, `false` the playlist is private, `null` the playlist status is not relevant. For more about public/private status, see [Working with Playlists](/documentation/web-api/concepts/playlists) |
| `snapshotId` | `string \| undefined` | Optional | The version identifier for the current playlist. Can be supplied in other requests to target a specific playlist version |
| `tracks` | [`PlaylistTracksRefObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/playlist-tracks-ref-object.md) | Optional | A collection containing a link ( `href` ) to the Web API endpoint where full details of the playlist's tracks can be retrieved, along with the `total` number of tracks in the playlist. Note, a track object may be `null`. This can happen if a track is no longer available. |
| `type` | `string \| undefined` | Optional | The object type: "playlist" |
| `uri` | `string \| undefined` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the playlist. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  SimplifiedPlaylistObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const simplifiedPlaylistObject: SimplifiedPlaylistObject = {
  collaborative: false,
  description: 'description0',
  externalUrls: {
    spotify: 'spotify6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  href: 'href8',
  id: 'id0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



