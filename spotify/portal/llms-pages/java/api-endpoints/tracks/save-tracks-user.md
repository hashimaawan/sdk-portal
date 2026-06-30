# Save-Tracks-User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0ZSUyRlRyYWNrcyUyRnNhdmUtdHJhY2tzLXVzZXI

Save one or more tracks to the current user's 'Your Music' library.

```java
CompletableFuture<ApiResponse<Void>> saveTracksUserAsync(
    final String ids,
    final MeTracksRequest body)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `String` | Query, Required | - |
| `body` | [`MeTracksRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/structures/me-tracks-request.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`user-library-modify`


# Response Type

**200**: Track saved

`void`


# Example Usage

```java
String ids = "7ouMYWpwJ422jRcDASZB7P,4VqPOruhp5EdPBeR92t6lQ,2takcwOaAZWiXQijPHIx7B";
tracksApi.saveTracksUserAsync(ids, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof UnauthorizedException) {
        UnauthorizedException unauthorizedException = (UnauthorizedException) cause;
        unauthorizedException.printStackTrace();
    } else if (cause instanceof ForbiddenException) {
        ForbiddenException forbiddenException = (ForbiddenException) cause;
        forbiddenException.printStackTrace();
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/exceptions/too-many-requests.md) |



