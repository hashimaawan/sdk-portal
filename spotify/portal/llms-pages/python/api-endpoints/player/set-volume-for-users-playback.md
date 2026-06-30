# Set-Volume-for-Users-Playback

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0ZSUyRlBsYXllciUyRnNldC12b2x1bWUtZm9yLXVzZXJzLXBsYXliYWNr

Set the volume for the user’s current playback device. This API only works for users who have Spotify Premium. The order of execution is not guaranteed when you use this API with other Player API endpoints.

```python
def set_volume_for_users_playback(self,
                                 volume_percent,
                                 device_id=None)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume_percent` | `int` | Query, Required | - |
| `device_id` | `str` | Query, Optional | - |


# Requires scope

## oauth_2_0

`user-modify-playback-state`


# Response Type

**204**: Command sent

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
volume_percent = 50

device_id = '0d1841b0976bae2a3a310dd74c0f3df354899bc8'

result = player_api.set_volume_for_users_playback(
    volume_percent,
    device_id=device_id
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



