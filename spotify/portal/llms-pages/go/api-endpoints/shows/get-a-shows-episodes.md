# Get-a-Shows-Episodes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0ZSUyRlNob3dzJTJGZ2V0LWEtc2hvd3MtZXBpc29kZXM

Get Spotify catalog information about an show’s episodes. Optional parameters can be used to limit the number of episodes returned.

```go
GetAShowsEpisodes(
    ctx context.Context,
    id string,
    market *string,
    limit *int,
    offset *int) (
    models.ApiResponse[models.PagingSimplifiedEpisodeObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | - |
| `market` | `*string` | Query, Optional | - |
| `limit` | `*int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |
| `offset` | `*int` | Query, Optional | **Default**: `0` |


# Requires scope

## oauth_2_0

`user-read-playback-position`


# Response Type

**200**: Pages of episodes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PagingSimplifiedEpisodeObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/paging-simplified-episode-object.md).


# Example Usage

```go
ctx := context.Background()

id := "38bS44xjbVVZ3No3ByF1dJ"

market := "ES"

limit := 10

offset := 5

apiResponse, err := showsApi.GetAShowsEpisodes(ctx, id, &market, &limit, &offset)
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



