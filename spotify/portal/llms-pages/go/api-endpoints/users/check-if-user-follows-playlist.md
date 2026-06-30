# Check-if-User-Follows-Playlist

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0ZSUyRlVzZXJzJTJGY2hlY2staWYtdXNlci1mb2xsb3dzLXBsYXlsaXN0

Check to see if one or more Spotify users are following a specified playlist.

```go
CheckIfUserFollowsPlaylist(
    ctx context.Context,
    playlistId string,
    ids string) (
    models.ApiResponse[[]bool],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `string` | Template, Required | - |
| `ids` | `string` | Query, Required | - |


# Response Type

**200**: Array of booleans

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type []bool.


# Example Usage

```go
ctx := context.Background()

playlistId := "3cEYpjA9oz9GiPac4AsH4n"

ids := "jmperezperez,thelinmichael,wizzler"

apiResponse, err := usersApi.CheckIfUserFollowsPlaylist(ctx, playlistId, ids)
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/too-many-requests.md) |



