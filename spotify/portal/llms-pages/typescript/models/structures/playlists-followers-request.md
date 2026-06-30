# Playlists Followers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwRm9sbG93ZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`PlaylistsFollowersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mPublic` | `boolean \| undefined` | Optional | Defaults to `true`. If `true` the playlist will be included in user's public playlists, if `false` it will remain private. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PlaylistsFollowersRequest,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const playlistsFollowersRequest: PlaylistsFollowersRequest = {
  mPublic: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



