# Get-Users-Top-Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0ZSUyRlVzZXJzJTJGZ2V0LXVzZXJzLXRvcC1hcnRpc3Rz

Get the current user's top artists based on calculated affinity.

```go
GetUsersTopArtists(
    ctx context.Context,
    timeRange *string,
    limit *int,
    offset *int) (
    models.ApiResponse[models.PagingArtistObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `timeRange` | `*string` | Query, Optional | **Default**: `"medium_term"` |
| `limit` | `*int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |
| `offset` | `*int` | Query, Optional | **Default**: `0` |


# Requires scope

## oauth_2_0

`user-top-read`


# Response Type

**200**: Pages of artists

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PagingArtistObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/paging-artist-object.md).


# Example Usage

```go
ctx := context.Background()

timeRange := "medium_term"

limit := 10

offset := 5

apiResponse, err := usersApi.GetUsersTopArtists(ctx, &timeRange, &limit, &offset)
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



