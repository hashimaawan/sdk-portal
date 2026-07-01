# Playergamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmdhbWVsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function playergamelogGet(string $playerId, string $season, string $seasonType): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$playerId = 'PlayerID6';

$season = 'Season0';

$seasonType = 'SeasonType8';

$api = $client->getAPI();
$apiResponse = $api->playergamelogGet(
    $playerId,
    $season,
    $seasonType
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



