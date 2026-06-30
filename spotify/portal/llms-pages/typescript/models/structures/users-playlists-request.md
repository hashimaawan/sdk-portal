# Users Playlists Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlVzZXJzJTI1MjBQbGF5bGlzdHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`UsersPlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | The name for the new playlist, for example `"Your Coolest Playlist"`. This name does not need to be unique; a user may have several playlists with the same name. |
| `mPublic` | `boolean \| undefined` | Optional | Defaults to `true`. If `true` the playlist will be public, if `false` it will be private. To be able to create private playlists, the user must have granted the `playlist-modify-private` [scope](/documentation/web-api/concepts/scopes/#list-of-scopes) |
| `collaborative` | `boolean \| undefined` | Optional | Defaults to `false`. If `true` the playlist will be collaborative. _**Note**: to create a collaborative playlist you must also set `public` to `false`. To create collaborative playlists you must have granted `playlist-modify-private` and `playlist-modify-public` [scopes](/documentation/web-api/concepts/scopes/#list-of-scopes)._ |
| `description` | `string \| undefined` | Optional | value for playlist description as displayed in Spotify Clients and in the Web API. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  UsersPlaylistsRequest,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const usersPlaylistsRequest: UsersPlaylistsRequest = {
  name: 'New Playlist',
  mPublic: false,
  collaborative: false,
  description: 'New playlist description',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



