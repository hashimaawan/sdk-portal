# Reorder-or-Replace-Playlists-Tracks

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRnJlb3JkZXItb3ItcmVwbGFjZS1wbGF5bGlzdHMtdHJhY2tz

Either reorder or replace items in a playlist depending on the request's parameters.
To reorder items, include `range_start`, `insert_before`, `range_length` and `snapshot_id` in the request's body.
To replace items, include `uris` as either a query parameter or in the request's body.
Replacing items in a playlist will overwrite its existing items. This operation can be used for replacing or clearing items in a playlist.
<br/>
**Note**: Replace and reorder are mutually exclusive operations which share the same endpoint, but have different parameters.
These operations can't be applied together in a single request.

```go
ReorderOrReplacePlaylistsTracks(
    ctx context.Context,
    playlistId string,
    uris *string,
    body *models.PlaylistsTracksRequest1) (
    models.ApiResponse[models.PlaylistSnapshotId],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `string` | Template, Required | - |
| `uris` | `*string` | Query, Optional | - |
| `body` | [`*models.PlaylistsTracksRequest1`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/playlists-tracks-request-1.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`playlist-modify-private`, `playlist-modify-public`


# Response Type

**200**: A snapshot ID for the playlist

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PlaylistSnapshotId](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/playlist-snapshot-id.md).


# Example Usage

```go
ctx := context.Background()

playlistId := "3cEYpjA9oz9GiPac4AsH4n"

body := models.PlaylistsTracksRequest1{
    RangeStart:            models.ToPointer(1),
    InsertBefore:          models.ToPointer(3),
    RangeLength:           models.ToPointer(2),
}

apiResponse, err := playlistsApi.ReorderOrReplacePlaylistsTracks(ctx, playlistId, nil, &body)
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



