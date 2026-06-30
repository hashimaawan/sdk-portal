# Get-Information-about-the-Users-Current-Playback

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0ZSUyRlBsYXllciUyRmdldC1pbmZvcm1hdGlvbi1hYm91dC10aGUtdXNlcnMtY3VycmVudC1wbGF5YmFjaw

Get information about the user’s current playback state, including track or episode, progress, and active device.

```csharp
GetInformationAboutTheUsersCurrentPlaybackAsync(
    string market = null,
    string additionalTypes = null)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `market` | `string` | Query, Optional | - |
| `additionalTypes` | `string` | Query, Optional | - |


# Requires scope

## oauth_2_0

`user-read-playback-state`


# Response Type

**200**: Information about playback

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.CurrentlyPlayingContextObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/currently-playing-context-object.md).


# Example Usage

```csharp
string market = "ES";
try
{
    ApiResponse<CurrentlyPlayingContextObject> result = await playerApi.GetInformationAboutTheUsersCurrentPlaybackAsync(market);
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



