# Get-Followed

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0ZSUyRlVzZXJzJTJGZ2V0LWZvbGxvd2Vk

Get the current user's followed artists.

```python
def get_followed(self,
                mtype,
                after=None,
                limit=20)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`ItemType1`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/enumerations/item-type-1.md) | Query, Required | - |
| `after` | `str` | Query, Optional | - |
| `limit` | `int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |


# Requires scope

## oauth_2_0

`user-follow-read`


# Response Type

**200**: A paged set of artists

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`CursorPagedArtists`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/cursor-paged-artists.md).


# Example Usage

```python
mtype = ItemType1.ARTIST

after = '0I2XqVXqHScXjHhk6AYYRe'

limit = 10

result = users_api.get_followed(
    mtype,
    after=after,
    limit=limit
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



