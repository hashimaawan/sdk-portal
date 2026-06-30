# Follow-Artists-Users

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0ZSUyRlVzZXJzJTJGZm9sbG93LWFydGlzdHMtdXNlcnM

Add the current user as a follower of one or more artists or other Spotify users.

```php
function followArtistsUsers(string $type, string $ids, ?MeFollowingRequest $body = null): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`string(ItemType2)`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/enumerations/item-type-2.md) | Query, Required | - |
| `ids` | `string` | Query, Required | - |
| `body` | [`?MeFollowingRequest`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/me-following-request.md) | Body, Optional | - |


# Requires scope

## oauth_2_0

`user-follow-modify`


# Response Type

**204**: Artist or user followed

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$type = ItemType2::ARTIST;

$ids = '2CIMQHirSU0MQqyYHq0eOx,57dN52uHvrHOxijzpIgu3E,1vCWHaC5f2uS3yhpwWbIA6';

$usersApi = $client->getUsersApi();
$apiResponse = $usersApi->followArtistsUsers(
    $type,
    $ids
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/exceptions/too-many-requests.md) |



