# Leagueleaders GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWxlYWRlcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function leagueleadersGet(
    string $leagueId,
    string $perMode,
    string $season,
    string $seasonType,
    string $scope,
    ?string $statCategory = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `scope` | `string` | Query, Required | - |
| `statCategory` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$leagueId = 'LeagueID4';

$perMode = 'PerMode6';

$season = 'Season0';

$seasonType = 'SeasonType8';

$scope = 'Scope0';

$api = $client->getAPI();
$apiResponse = $api->leagueleadersGet(
    $leagueId,
    $perMode,
    $season,
    $seasonType,
    $scope
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



