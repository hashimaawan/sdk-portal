# Get-Users-Saved-Shows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0ZSUyRlNob3dzJTJGZ2V0LXVzZXJzLXNhdmVkLXNob3dz

Get a list of shows saved in the current Spotify user's library. Optional parameters can be used to limit the number of shows returned.

```java
CompletableFuture<ApiResponse<PagingSavedShowObject>> getUsersSavedShowsAsync(
    final Integer limit,
    final Integer offset)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `Integer` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |
| `offset` | `Integer` | Query, Optional | **Default**: `0` |


# Requires scope

## oauth_2_0

`user-library-read`


# Response Type

**200**: Pages of shows

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PagingSavedShowObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/structures/paging-saved-show-object.md).


# Example Usage

```java
Integer limit = 10;
Integer offset = 5;

showsApi.getUsersSavedShowsAsync(limit, offset).thenAccept(result -> {
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



