# Get-Queue

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0ZSUyRlBsYXllciUyRmdldC1xdWV1ZQ

Get the list of objects that make up the user's queue.

```csharp
GetQueueAsync()
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Requires scope

## oauth_2_0

`user-read-currently-playing`, `user-read-playback-state`


# Response Type

**200**: Information about the queue

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.QueueObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/queue-object.md).


# Example Usage

```csharp
try
{
    ApiResponse<QueueObject> result = await playerApi.GetQueueAsync();
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/exceptions/too-many-requests.md) |



