# Get-Information-about-the-Users-Current-Playback

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0ZSUyRlBsYXllciUyRmdldC1pbmZvcm1hdGlvbi1hYm91dC10aGUtdXNlcnMtY3VycmVudC1wbGF5YmFjaw

Get information about the user’s current playback state, including track or episode, progress, and active device.

```php
function getInformationAboutTheUsersCurrentPlayback(
    ?string $market = null,
    ?string $additionalTypes = null
): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `market` | `?string` | Query, Optional | - |
| `additionalTypes` | `?string` | Query, Optional | - |


# Requires scope

## oauth_2_0

`user-read-playback-state`


# Response Type

**200**: Information about playback

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CurrentlyPlayingContextObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/currently-playing-context-object.md).


# Example Usage

```php
$market = 'ES';

$playerApi = $client->getPlayerApi();
$apiResponse = $playerApi->getInformationAboutTheUsersCurrentPlayback($market);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CurrentlyPlayingContextObject:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/too-many-requests.md) |



