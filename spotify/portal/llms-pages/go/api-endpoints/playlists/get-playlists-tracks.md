# Get-Playlists-Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmdldC1wbGF5bGlzdHMtdHJhY2tz

Get full details of the items of a playlist owned by a Spotify user.

```go
GetPlaylistsTracks(
    ctx context.Context,
    playlistId string,
    market *string,
    fields *string,
    limit *int,
    offset *int,
    additionalTypes *string) (
    models.ApiResponse[models.PagingPlaylistTrackObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `string` | Template, Required | - |
| `market` | `*string` | Query, Optional | - |
| `fields` | `*string` | Query, Optional | - |
| `limit` | `*int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `offset` | `*int` | Query, Optional | **Default**: `0` |
| `additionalTypes` | `*string` | Query, Optional | - |


# Requires scope

## oauth_2_0

`playlist-read-private`


# Response Type

**200**: Pages of tracks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PagingPlaylistTrackObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/paging-playlist-track-object.md).


# Example Usage

```go
ctx := context.Background()

playlistId := "3cEYpjA9oz9GiPac4AsH4n"

market := "ES"

fields := "items(added_by.id,track(name,href,album(name,href)))"

limit := 10

offset := 5

apiResponse, err := playlistsApi.GetPlaylistsTracks(ctx, playlistId, &market, &fields, &limit, &offset, nil)
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



