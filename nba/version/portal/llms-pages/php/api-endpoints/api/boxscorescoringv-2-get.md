# Boxscorescoringv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkJveHNjb3Jlc2NvcmluZ3YyX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function boxscorescoringv2Get(
    string $gameId,
    string $startPeriod,
    string $endPeriod,
    string $startRange,
    string $endRange,
    string $rangeType
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameId` | `string` | Query, Required | - |
| `startPeriod` | `string` | Query, Required | - |
| `endPeriod` | `string` | Query, Required | - |
| `startRange` | `string` | Query, Required | - |
| `endRange` | `string` | Query, Required | - |
| `rangeType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$gameId = 'GameID8';

$startPeriod = 'StartPeriod4';

$endPeriod = 'EndPeriod0';

$startRange = 'StartRange0';

$endRange = 'EndRange2';

$rangeType = 'RangeType0';

$api = $client->getAPI();
$apiResponse = $api->boxscorescoringv2Get(
    $gameId,
    $startPeriod,
    $endPeriod,
    $startRange,
    $endRange,
    $rangeType
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
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



