# Get-Playlists-Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmdldC1wbGF5bGlzdHMtdHJhY2tz

Get full details of the items of a playlist owned by a Spotify user.

```java
CompletableFuture<ApiResponse<PagingPlaylistTrackObject>> getPlaylistsTracksAsync(
    final String playlistId,
    final String market,
    final String fields,
    final Integer limit,
    final Integer offset,
    final String additionalTypes)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `String` | Template, Required | - |
| `market` | `String` | Query, Optional | - |
| `fields` | `String` | Query, Optional | - |
| `limit` | `Integer` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `offset` | `Integer` | Query, Optional | **Default**: `0` |
| `additionalTypes` | `String` | Query, Optional | - |


# Requires scope

## oauth_2_0

`playlist-read-private`


# Response Type

**200**: Pages of tracks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PagingPlaylistTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/structures/paging-playlist-track-object.md).


# Example Usage

```java
String playlistId = "3cEYpjA9oz9GiPac4AsH4n";
String market = "ES";
String fields = "items(added_by.id,track(name,href,album(name,href)))";
Integer limit = 10;
Integer offset = 5;

playlistsApi.getPlaylistsTracksAsync(playlistId, market, fields, limit, offset, null).thenAccept(result -> {
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



