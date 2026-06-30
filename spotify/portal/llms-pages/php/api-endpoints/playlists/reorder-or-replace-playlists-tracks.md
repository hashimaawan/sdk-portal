# Reorder-or-Replace-Playlists-Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0ZSUyRlBsYXlsaXN0cyUyRnJlb3JkZXItb3ItcmVwbGFjZS1wbGF5bGlzdHMtdHJhY2tz

Either reorder or replace items in a playlist depending on the request's parameters.
To reorder items, include `range_start`, `insert_before`, `range_length` and `snapshot_id` in the request's body.
To replace items, include `uris` as either a query parameter or in the request's body.
Replacing items in a playlist will overwrite its existing items. This operation can be used for replacing or clearing items in a playlist.
<br/>
**Note**: Replace and reorder are mutually exclusive operations which share the same endpoint, but have different parameters.
These operations can't be applied together in a single request.

```php
function reorderOrReplacePlaylistsTracks(
    string $playlistId,
    ?string $uris = null,
    ?PlaylistsTracksRequest1 $body = null
): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playlistId` | `string` | Template, Required | - |
| `uris` | `?string` | Query, Optional | - |
| `body` | [`?PlaylistsTracksRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/playlists-tracks-request-1.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`playlist-modify-private`, `playlist-modify-public`


# Response Type

**200**: A snapshot ID for the playlist

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PlaylistSnapshotId`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/playlist-snapshot-id.md).


# Example Usage

```php
$playlistId = '3cEYpjA9oz9GiPac4AsH4n';

$body = PlaylistsTracksRequest1Builder::init()
    ->rangeStart(1)
    ->insertBefore(3)
    ->rangeLength(2)
    ->build();

$playlistsApi = $client->getPlaylistsApi();
$apiResponse = $playlistsApi->reorderOrReplacePlaylistsTracks(
    $playlistId,
    null,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PlaylistSnapshotId:';
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



