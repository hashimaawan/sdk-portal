# Change-Playlist-Details

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmNoYW5nZS1wbGF5bGlzdC1kZXRhaWxz

Change a playlist's name and public/private state. (The user must, of
course, own the playlist.)

```csharp
ChangePlaylistDetailsAsync(
    string playlistId,
    Models.PlaylistsRequest body = null)
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `string` | Template, Required | - |
| `body` | [`PlaylistsRequest`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/playlists-request.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`playlist-modify-private`, `playlist-modify-public`


# Response Type

**200**: Playlist updated

`Task`


# Example Usage

```csharp
string playlistId = "3cEYpjA9oz9GiPac4AsH4n";
PlaylistsRequest body = new PlaylistsRequest
{
    Name = "Updated Playlist Name",
    MPublic = false,
    Description = "Updated playlist description",
};

try
{
    await playlistsApi.ChangePlaylistDetailsAsync(
        playlistId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is UnauthorizedException)
    {
       // TODO: Handle UnauthorizedException exception here
    }
    if (e is ForbiddenException)
    {
       // TODO: Handle ForbiddenException exception here
    }
    if (e is TooManyRequestsException)
    {
       // TODO: Handle TooManyRequestsException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/exceptions/too-many-requests.md) |



