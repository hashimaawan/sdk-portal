# Playlists Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`PlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The new name for the playlist, for example `"My New Playlist Title"` |
| `mPublic` | `boolean \| undefined` | Optional | If `true` the playlist will be public, if `false` it will be private. |
| `collaborative` | `boolean \| undefined` | Optional | If `true`, the playlist will become collaborative and other users will be able to modify the playlist in their Spotify client. <br/><br>_**Note**: You can only set `collaborative` to `true` on non-public playlists._ |
| `description` | `string \| undefined` | Optional | Value for playlist description as displayed in Spotify Clients and in the Web API. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PlaylistsRequest,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const playlistsRequest: PlaylistsRequest = {
  name: 'Updated Playlist Name',
  mPublic: false,
  collaborative: false,
  description: 'Updated playlist description',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



