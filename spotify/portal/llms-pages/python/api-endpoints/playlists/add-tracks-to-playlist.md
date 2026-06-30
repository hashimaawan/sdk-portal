# Add-Tracks-to-Playlist

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmFkZC10cmFja3MtdG8tcGxheWxpc3Q

Add one or more items to a user's playlist.

```python
def add_tracks_to_playlist(self,
                          playlist_id,
                          position=None,
                          uris=None,
                          body=None)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlist_id` | `str` | Template, Required | - |
| `position` | `int` | Query, Optional | - |
| `uris` | `str` | Query, Optional | - |
| `body` | [`PlaylistsTracksRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/playlists-tracks-request.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`playlist-modify-private`, `playlist-modify-public`


# Response Type

**201**: A snapshot ID for the playlist

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`PlaylistSnapshotId`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/playlist-snapshot-id.md).


# Example Usage

```python
playlist_id = '3cEYpjA9oz9GiPac4AsH4n'

position = 0

uris = 'spotify:track:4iV5W9uYEdYUVa79Axb7Rh,spotify:track:1301WleyT98MSxVHPZCA6M'

result = playlists_api.add_tracks_to_playlist(
    playlist_id,
    position=position,
    uris=uris
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/too-many-requests.md) |



