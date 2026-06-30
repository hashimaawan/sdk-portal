# Get-an-Audiobook

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0ZSUyRkF1ZGlvYm9va3MlMkZnZXQtYW4tYXVkaW9ib29r

Get Spotify catalog information for a single audiobook. Audiobooks are only available within the US, UK, Canada, Ireland, New Zealand and Australia markets.

```java
CompletableFuture<ApiResponse<AudiobookObject>> getAnAudiobookAsync(
    final String id,
    final String market)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | - |
| `market` | `String` | Query, Optional | - |


# Response Type

**200**: An Audiobook

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`AudiobookObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/audiobook-object.md).


# Example Usage

```java
String id = "7iHfbu1YPACw6oZPAFJtqe";
String market = "ES";

audiobooksApi.getAnAudiobookAsync(id, market).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof BadRequestException) {
        BadRequestException badRequestException = (BadRequestException) cause;
        badRequestException.printStackTrace();
    } else if (cause instanceof UnauthorizedException) {
        UnauthorizedException unauthorizedException = (UnauthorizedException) cause;
        unauthorizedException.printStackTrace();
    } else if (cause instanceof ForbiddenException) {
        ForbiddenException forbiddenException = (ForbiddenException) cause;
        forbiddenException.printStackTrace();
    } else if (cause instanceof NotFoundException) {
        NotFoundException notFoundException = (NotFoundException) cause;
        notFoundException.printStackTrace();
    } else if (cause instanceof TooManyRequestsException) {
        TooManyRequestsException tooManyRequestsException = (TooManyRequestsException) cause;
        tooManyRequestsException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | The request contains malformed data in path, query parameters, or body. | [`BadRequestException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/bad-request.md) |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/forbidden.md) |
| 404 | The requested resource cannot be found. | [`NotFoundException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/not-found.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/too-many-requests.md) |



