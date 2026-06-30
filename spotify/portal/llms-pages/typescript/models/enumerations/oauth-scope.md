# OAuth Scope

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk9BdXRoJTI1MjBTY29wZQ

OAuth 2 scopes supported by the API


# Enum Type Name

`OauthScope`


# Fields

| Name | Description |
|  --- | --- |
| `AppRemoteControl` | Communicate with the Spotify app on your device. |
| `PlaylistReadPrivate` | Access your private playlists. |
| `PlaylistReadCollaborative` | Access your collaborative playlists. |
| `PlaylistModifyPublic` | Manage your public playlists. |
| `PlaylistModifyPrivate` | Manage your private playlists. |
| `UserLibraryRead` | Access your saved content. |
| `UserLibraryModify` | Manage your saved content. |
| `UserReadPrivate` | Access your subscription details. |
| `UserReadEmail` | Get your real email address. |
| `UserFollowRead` | Access your followers and who you are following. |
| `UserFollowModify` | Manage your saved content. |
| `UserTopRead` | Read your top artists and content. |
| `UserReadPlaybackPosition` | Read your position in content you have played. |
| `UserReadPlaybackState` | Read your currently playing content and Spotify Connect devices information. |
| `UserReadRecentlyPlayed` | Access your recently played items. |
| `UserReadCurrentlyPlaying` | Read your currently playing content. |
| `UserModifyPlaybackState` | Control playback on your Spotify clients and Spotify Connect devices. |
| `UgcImageUpload` | Upload images to Spotify on your behalf. |
| `Streaming` | Play content and control playback on your other devices. |


# Example

```ts
import {
  OauthScope,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const oauthScope = OauthScope.UserLibraryRead;
```



