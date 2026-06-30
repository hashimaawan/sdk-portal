# Get-an-Audiobook

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0ZSUyRkF1ZGlvYm9va3MlMkZnZXQtYW4tYXVkaW9ib29r

Get Spotify catalog information for a single audiobook. Audiobooks are only available within the US, UK, Canada, Ireland, New Zealand and Australia markets.

```go
GetAnAudiobook(
    ctx context.Context,
    id string,
    market *string) (
    models.ApiResponse[models.AudiobookObject],
    error)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | - |
| `market` | `*string` | Query, Optional | - |


# Response Type

**200**: An Audiobook

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.AudiobookObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/audiobook-object.md).


# Example Usage

```go
ctx := context.Background()

id := "7iHfbu1YPACw6oZPAFJtqe"

market := "ES"

apiResponse, err := audiobooksApi.GetAnAudiobook(ctx, id, &market)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.BadRequest:
            log.Fatalln("BadRequestException: ", typedErr)
        case *errors.Unauthorized:
            log.Fatalln("UnauthorizedException: ", typedErr)
        case *errors.Forbidden:
            log.Fatalln("ForbiddenException: ", typedErr)
        case *errors.NotFound:
            log.Fatalln("NotFoundException: ", typedErr)
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
| 400 | The request contains malformed data in path, query parameters, or body. | [`BadRequestException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/bad-request.md) |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/forbidden.md) |
| 404 | The requested resource cannot be found. | [`NotFoundException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/not-found.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/exceptions/too-many-requests.md) |



