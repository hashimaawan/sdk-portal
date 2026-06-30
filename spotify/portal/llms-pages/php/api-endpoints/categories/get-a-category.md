# Get-a-Category

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0ZSUyRkNhdGVnb3JpZXMlMkZnZXQtYS1jYXRlZ29yeQ

Get a single category used to tag items in Spotify (on, for example, the Spotify player’s “Browse” tab).

```php
function getACategory(string $categoryId, ?string $locale = null): ApiResponse
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categoryId` | `string` | Template, Required | - |
| `locale` | `?string` | Query, Optional | - |


# Response Type

**200**: A category

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CategoryObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/category-object.md).


# Example Usage

```php
$categoryId = 'dinner';

$locale = 'sv_SE';

$categoriesApi = $client->getCategoriesApi();
$apiResponse = $categoriesApi->getACategory(
    $categoryId,
    $locale
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CategoryObject:';
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



