# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function playerdashptshotlogGet(
    ?string $leagueId = null,
    ?string $season = null,
    ?string $seasonType = null,
    ?string $playerId = null,
    ?string $teamId = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `?string` | Query, Optional | - |
| `season` | `?string` | Query, Optional | - |
| `seasonType` | `?string` | Query, Optional | - |
| `playerId` | `?string` | Query, Optional | - |
| `teamId` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$api = $client->getAPI();
$apiResponse = $api->playerdashptshotlogGet();

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



