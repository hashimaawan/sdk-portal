# Check-if-User-Follows-Playlist

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0ZSUyRlVzZXJzJTJGY2hlY2staWYtdXNlci1mb2xsb3dzLXBsYXlsaXN0

Check to see if one or more Spotify users are following a specified playlist.

```ruby
def check_if_user_follows_playlist(playlist_id,
                                   ids)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlist_id` | `String` | Template, Required | - |
| `ids` | `String` | Query, Required | - |


# Response Type

**200**: Array of booleans

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type `Array[TrueClass | FalseClass]`.


# Example Usage

```ruby
playlist_id = '3cEYpjA9oz9GiPac4AsH4n'

ids = 'jmperezperez,thelinmichael,wizzler'

result = users_api.check_if_user_follows_playlist(
  playlist_id,
  ids
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response

```
[
  false,
  true
]
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/exceptions/too-many-requests.md) |



