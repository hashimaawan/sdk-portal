# Unfollow-Artists-Users

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0ZSUyRlVzZXJzJTJGdW5mb2xsb3ctYXJ0aXN0cy11c2Vycw

Remove the current user as a follower of one or more artists or other Spotify users.

```python
def unfollow_artists_users(self,
                          mtype,
                          ids,
                          body=None)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`ItemType3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/item-type-3.md) | Query, Required | - |
| `ids` | `str` | Query, Required | - |
| `body` | [`MeFollowingRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/me-following-request-1.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`user-follow-modify`


# Response Type

**200**: Artist or user unfollowed

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
mtype = ItemType3.ARTIST

ids = '2CIMQHirSU0MQqyYHq0eOx,57dN52uHvrHOxijzpIgu3E,1vCWHaC5f2uS3yhpwWbIA6'

result = users_api.unfollow_artists_users(
    mtype,
    ids
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



