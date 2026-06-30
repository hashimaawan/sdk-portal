# Get-Playlists-Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmdldC1wbGF5bGlzdHMtdHJhY2tz

Get full details of the items of a playlist owned by a Spotify user.

```python
def get_playlists_tracks(self,
                        playlist_id,
                        market=None,
                        fields=None,
                        limit=20,
                        offset=0,
                        additional_types=None)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlist_id` | `str` | Template, Required | - |
| `market` | `str` | Query, Optional | - |
| `fields` | `str` | Query, Optional | - |
| `limit` | `int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `offset` | `int` | Query, Optional | **Default**: `0` |
| `additional_types` | `str` | Query, Optional | - |


# Requires scope

## oauth_2_0

`playlist-read-private`


# Response Type

**200**: Pages of tracks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`PagingPlaylistTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/paging-playlist-track-object.md).


# Example Usage

```python
playlist_id = '3cEYpjA9oz9GiPac4AsH4n'

market = 'ES'

fields = 'items(added_by.id,track(name,href,album(name,href)))'

limit = 10

offset = 5

result = playlists_api.get_playlists_tracks(
    playlist_id,
    market=market,
    fields=fields,
    limit=limit,
    offset=offset
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



