# Get-Multiple-Shows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0ZSUyRlNob3dzJTJGZ2V0LW11bHRpcGxlLXNob3dz

Get Spotify catalog information for several shows based on their Spotify IDs.

```go
GetMultipleShows(
    ctx context.Context,
    ids string,
    market *string) (
    models.ApiResponse[models.ManySimplifiedShows],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `string` | Query, Required | - |
| `market` | `*string` | Query, Optional | - |


# Response Type

**200**: A set of shows

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ManySimplifiedShows](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/many-simplified-shows.md).


# Example Usage

```go
ctx := context.Background()

ids := "5CfCWKI5pZ28U0uOzXkDHe,5as3aKmN2k11yfDDDSrvaZ"

market := "ES"

apiResponse, err := showsApi.GetMultipleShows(ctx, ids, &market)
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



