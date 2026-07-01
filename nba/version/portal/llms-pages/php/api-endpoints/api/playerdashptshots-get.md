# Playerdashptshots GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3RzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function playerdashptshotsGet(
    string $perMode,
    string $season,
    string $seasonType,
    string $playerId,
    string $teamId,
    string $outcome,
    string $location,
    string $month,
    string $seasonSegment,
    string $dateFrom,
    string $dateTo,
    string $opponentTeamId,
    string $vsConference,
    string $vsDivision,
    string $gameSegment,
    string $period,
    string $lastNGames
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerId` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamId` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$perMode = 'PerMode6';

$season = 'Season0';

$seasonType = 'SeasonType8';

$playerId = 'PlayerID6';

$teamId = 'TeamID8';

$outcome = 'Outcome4';

$location = 'Location4';

$month = 'Month0';

$seasonSegment = 'SeasonSegment8';

$dateFrom = 'DateFrom6';

$dateTo = 'DateTo0';

$opponentTeamId = 'OpponentTeamID6';

$vsConference = 'VsConference6';

$vsDivision = 'VsDivision6';

$gameSegment = 'GameSegment6';

$period = 'Period2';

$lastNGames = 'LastNGames4';

$api = $client->getAPI();
$apiResponse = $api->playerdashptshotsGet(
    $perMode,
    $season,
    $seasonType,
    $playerId,
    $teamId,
    $outcome,
    $location,
    $month,
    $seasonSegment,
    $dateFrom,
    $dateTo,
    $opponentTeamId,
    $vsConference,
    $vsDivision,
    $gameSegment,
    $period,
    $lastNGames
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



