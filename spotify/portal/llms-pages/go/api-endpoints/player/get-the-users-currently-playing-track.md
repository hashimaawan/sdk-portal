# Get-the-Users-Currently-Playing-Track

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0ZSUyRlBsYXllciUyRmdldC10aGUtdXNlcnMtY3VycmVudGx5LXBsYXlpbmctdHJhY2s

Get the object currently being played on the user's Spotify account.

```go
GetTheUsersCurrentlyPlayingTrack(
    ctx context.Context,
    market *string,
    additionalTypes *string) (
    models.ApiResponse[models.CurrentlyPlayingObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `market` | `*string` | Query, Optional | - |
| `additionalTypes` | `*string` | Query, Optional | - |


# Requires scope

## oauth_2_0

`user-read-currently-playing`


# Response Type

**200**: Information about the currently playing track

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.CurrentlyPlayingObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/currently-playing-object.md).


# Example Usage

```go
ctx := context.Background()

market := "ES"

apiResponse, err := playerApi.GetTheUsersCurrentlyPlayingTrack(ctx, &market, nil)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.Unauthorized:
            log.Fatalln("UnauthorizedException: ", typedErr)
        case *errors.Forbidden:
            log.Fatalln("ForbiddenException: ", typedErr)
        case *errors.TooManyRequests:
            log.Fatalln("TooManyRequestsException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/too-many-requests.md) |



