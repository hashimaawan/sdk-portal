# Get-an-Albums-Tracks

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0ZSUyRkFsYnVtcyUyRmdldC1hbi1hbGJ1bXMtdHJhY2tz

Get Spotify catalog information about an album’s tracks.
Optional parameters can be used to limit the number of tracks returned.

```python
def get_an_albums_tracks(self,
                        id,
                        market=None,
                        limit=20,
                        offset=0)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Template, Required | - |
| `market` | `str` | Query, Optional | - |
| `limit` | `int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |
| `offset` | `int` | Query, Optional | **Default**: `0` |


# Response Type

**200**: Pages of tracks

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`PagingSimplifiedTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/paging-simplified-track-object.md).


# Example Usage

```python
id = '4aawyAB9vmqN3uQ7FjRGTy'

market = 'ES'

limit = 10

offset = 5

result = albums_api.get_an_albums_tracks(
    id,
    market=market,
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/exceptions/too-many-requests.md) |



