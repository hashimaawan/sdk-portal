# Get-Playlists-Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmdldC1wbGF5bGlzdHMtdHJhY2tz

Get full details of the items of a playlist owned by a Spotify user.

```ruby
def get_playlists_tracks(playlist_id,
                         market: nil,
                         fields: nil,
                         limit: 20,
                         offset: 0,
                         additional_types: nil)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlist_id` | `String` | Template, Required | - |
| `market` | `String` | Query, Optional | - |
| `fields` | `String` | Query, Optional | - |
| `limit` | `Integer` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `offset` | `Integer` | Query, Optional | **Default**: `0` |
| `additional_types` | `String` | Query, Optional | - |


# Requires scope

## oauth_2_0

`playlist-read-private`


# Response Type

**200**: Pages of tracks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`PagingPlaylistTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/paging-playlist-track-object.md).


# Example Usage

```ruby
playlist_id = '3cEYpjA9oz9GiPac4AsH4n'

market = 'ES'

fields = 'items(added_by.id,track(name,href,album(name,href)))'

limit = 10

offset = 5

result = playlists_api.get_playlists_tracks(
  playlist_id,
  market: market,
  fields: fields,
  limit: limit,
  offset: offset
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/exceptions/too-many-requests.md) |



