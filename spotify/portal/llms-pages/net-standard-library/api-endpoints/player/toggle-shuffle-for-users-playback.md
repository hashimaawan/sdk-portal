# Toggle-Shuffle-for-Users-Playback

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0ZSUyRlBsYXllciUyRnRvZ2dsZS1zaHVmZmxlLWZvci11c2Vycy1wbGF5YmFjaw

Toggle shuffle on or off for user’s playback. This API only works for users who have Spotify Premium. The order of execution is not guaranteed when you use this API with other Player API endpoints.

```csharp
ToggleShuffleForUsersPlaybackAsync(
    bool state,
    string deviceId = null)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | `bool` | Query, Required | - |
| `deviceId` | `string` | Query, Optional | - |


# Requires scope

## oauth_2_0

`user-modify-playback-state`


# Response Type

**204**: Command sent

`Task`


# Example Usage

```csharp
bool state = true;
string deviceId = "0d1841b0976bae2a3a310dd74c0f3df354899bc8";
try
{
    await playerApi.ToggleShuffleForUsersPlaybackAsync(
        state,
        deviceId
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is UnauthorizedException)
    {
       // TODO: Handle UnauthorizedException exception here
    }
    if (e is ForbiddenException)
    {
       // TODO: Handle ForbiddenException exception here
    }
    if (e is TooManyRequestsException)
    {
       // TODO: Handle TooManyRequestsException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/exceptions/too-many-requests.md) |



