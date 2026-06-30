# Create-Playlist

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmNyZWF0ZS1wbGF5bGlzdA

Create a playlist for a Spotify user. (The playlist will be empty until
you [add tracks](/documentation/web-api/reference/add-tracks-to-playlist).)
Each user is generally limited to a maximum of 11000 playlists.

```go
CreatePlaylist(
    ctx context.Context,
    userId string,
    body *models.UsersPlaylistsRequest) (
    models.ApiResponse[models.PlaylistObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `userId` | `string` | Template, Required | - |
| `body` | [`*models.UsersPlaylistsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/users-playlists-request.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`playlist-modify-private`, `playlist-modify-public`


# Response Type

**201**: A playlist

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PlaylistObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/playlist-object.md).


# Example Usage

```go
ctx := context.Background()

userId := "smedjan"

body := models.UsersPlaylistsRequest{
    Name:                  "New Playlist",
    Public:                models.ToPointer(false),
    Description:           models.ToPointer("New playlist description"),
}

apiResponse, err := playlistsApi.CreatePlaylist(ctx, userId, &body)
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/exceptions/too-many-requests.md) |



