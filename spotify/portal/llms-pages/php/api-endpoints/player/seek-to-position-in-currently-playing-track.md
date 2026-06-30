# Seek-to-Position-in-Currently-Playing-Track

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0ZSUyRlBsYXllciUyRnNlZWstdG8tcG9zaXRpb24taW4tY3VycmVudGx5LXBsYXlpbmctdHJhY2s

Seeks to the given position in the user’s currently playing track. This API only works for users who have Spotify Premium. The order of execution is not guaranteed when you use this API with other Player API endpoints.

```php
function seekToPositionInCurrentlyPlayingTrack(int $positionMs, ?string $deviceId = null): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `positionMs` | `int` | Query, Required | - |
| `deviceId` | `?string` | Query, Optional | - |


# Requires scope

## oauth_2_0

`user-modify-playback-state`


# Response Type

**204**: Command sent

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$positionMs = 25000;

$deviceId = '0d1841b0976bae2a3a310dd74c0f3df354899bc8';

$playerApi = $client->getPlayerApi();
$apiResponse = $playerApi->seekToPositionInCurrentlyPlayingTrack(
    $positionMs,
    $deviceId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
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



