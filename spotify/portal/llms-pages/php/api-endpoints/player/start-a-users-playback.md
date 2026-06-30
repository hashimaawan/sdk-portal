# Start-a-Users-Playback

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0ZSUyRlBsYXllciUyRnN0YXJ0LWEtdXNlcnMtcGxheWJhY2s

Start a new context or resume current playback on the user's active device. This API only works for users who have Spotify Premium. The order of execution is not guaranteed when you use this API with other Player API endpoints.

```php
function startAUsersPlayback(?string $deviceId = null, ?MePlayerPlayRequest $body = null): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deviceId` | `?string` | Query, Optional | - |
| `body` | [`?MePlayerPlayRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/me-player-play-request.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`user-modify-playback-state`


# Response Type

**204**: Playback started

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$deviceId = '0d1841b0976bae2a3a310dd74c0f3df354899bc8';

$body = MePlayerPlayRequestBuilder::init()
    ->contextUri('spotify:album:5ht7ItJgpBH7W6vJ5BqpPr')
    ->offset(ApiHelper::deserialize('{"position":5}'))
    ->positionMs(0)
    ->build();

$playerApi = $client->getPlayerApi();
$apiResponse = $playerApi->startAUsersPlayback(
    $deviceId,
    $body
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



