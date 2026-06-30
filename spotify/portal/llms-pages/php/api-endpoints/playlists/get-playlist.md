# Get-Playlist

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRmdldC1wbGF5bGlzdA

Get a playlist owned by a Spotify user.

```php
function getPlaylist(
    string $playlistId,
    ?string $market = null,
    ?string $fields = null,
    ?string $additionalTypes = null
): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `string` | Template, Required | - |
| `market` | `?string` | Query, Optional | - |
| `fields` | `?string` | Query, Optional | - |
| `additionalTypes` | `?string` | Query, Optional | - |


# Response Type

**200**: A playlist

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/playlist-object.md).


# Example Usage

```php
$playlistId = '3cEYpjA9oz9GiPac4AsH4n';

$market = 'ES';

$fields = 'items(added_by.id,track(name,href,album(name,href)))';

$playlistsApi = $client->getPlaylistsApi();
$apiResponse = $playlistsApi->getPlaylist(
    $playlistId,
    $market,
    $fields
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PlaylistObject:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/exceptions/too-many-requests.md) |



