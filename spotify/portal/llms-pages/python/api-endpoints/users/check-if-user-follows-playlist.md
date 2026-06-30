# Check-if-User-Follows-Playlist

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0ZSUyRlVzZXJzJTJGY2hlY2staWYtdXNlci1mb2xsb3dzLXBsYXlsaXN0

Check to see if one or more Spotify users are following a specified playlist.

```python
def check_if_user_follows_playlist(self,
                                  playlist_id,
                                  ids)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlist_id` | `str` | Template, Required | - |
| `ids` | `str` | Query, Required | - |


# Response Type

**200**: Array of booleans

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type `List[bool]`.


# Example Usage

```python
playlist_id = '3cEYpjA9oz9GiPac4AsH4n'

ids = 'jmperezperez,thelinmichael,wizzler'

result = users_api.check_if_user_follows_playlist(
    playlist_id,
    ids
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/too-many-requests.md) |



