# Boxscoreusage GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JldXNhZ2VfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function boxscoreusageGet(
    ?string $gameId = null,
    ?string $startPeriod = null,
    ?string $endPeriod = null,
    ?string $startRange = null,
    ?string $endRange = null,
    ?string $rangeType = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `?string` | Query, Optional | - |
| `startPeriod` | `?string` | Query, Optional | - |
| `endPeriod` | `?string` | Query, Optional | - |
| `startRange` | `?string` | Query, Optional | - |
| `endRange` | `?string` | Query, Optional | - |
| `rangeType` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$api = $client->getAPI();
$apiResponse = $api->boxscoreusageGet();

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
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



