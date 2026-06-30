# Remove-Tracks-Playlist

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRnJlbW92ZS10cmFja3MtcGxheWxpc3Q

Remove one or more items from a user's playlist.

```java
CompletableFuture<ApiResponse<PlaylistSnapshotId>> removeTracksPlaylistAsync(
    final String playlistId,
    final PlaylistsTracksRequest2 body)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `String` | Template, Required | - |
| `body` | [`PlaylistsTracksRequest2`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/playlists-tracks-request-2.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`playlist-modify-private`, `playlist-modify-public`


# Response Type

**200**: A snapshot ID for the playlist

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PlaylistSnapshotId`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/playlist-snapshot-id.md).


# Example Usage

```java
String playlistId = "3cEYpjA9oz9GiPac4AsH4n";
PlaylistsTracksRequest2 body = new PlaylistsTracksRequest2.Builder(
    Arrays.asList(
        new Track1.Builder()
            .build()
    )
)
.build();

playlistsApi.removeTracksPlaylistAsync(playlistId, body).thenAccept(result -> {
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/exceptions/too-many-requests.md) |



