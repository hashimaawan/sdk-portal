# Search

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0ZSUyRlNlYXJjaCUyRnNlYXJjaA

Get Spotify catalog information about albums, artists, playlists, tracks, shows, episodes or audiobooks
that match a keyword string. Audiobooks are only available within the US, UK, Canada, Ireland, New Zealand and Australia markets.

```python
def search(self,
          q,
          mtype,
          market=None,
          limit=20,
          offset=0,
          include_external=None)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `str` | Query, Required | - |
| `mtype` | [`List[ItemType]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/item-type.md) | Query, Required | - |
| `market` | `str` | Query, Optional | - |
| `limit` | `int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |
| `offset` | `int` | Query, Optional | **Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 1000` |
| `include_external` | [`IncludeExternal`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/include-external.md) | Query, Optional | - |


# Response Type

**200**: Search response

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`SearchItems`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/search-items.md).


# Example Usage

```python
q = 'remaster%20track:Doxy%20artist:Miles%20Davis'

mtype = [
    ItemType.AUDIOBOOK,
    ItemType.ALBUM,
    ItemType.ARTIST
]

market = 'ES'

limit = 10

offset = 5

result = search_api.search(
    q,
    mtype,
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/exceptions/too-many-requests.md) |



