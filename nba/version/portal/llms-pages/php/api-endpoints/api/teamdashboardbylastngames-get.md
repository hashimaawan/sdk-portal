# Teamdashboardbylastngames GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlRlYW1kYXNoYm9hcmRieWxhc3RuZ2FtZXNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function teamdashboardbylastngamesGet(
    string $teamId,
    string $measureType,
    string $perMode,
    string $plusMinus,
    string $paceAdjust,
    string $rank,
    string $season,
    string $seasonType,
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
| `teamId` | `string` | Query, Required | - |
| `measureType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `plusMinus` | `string` | Query, Required | - |
| `paceAdjust` | `string` | Query, Required | - |
| `rank` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
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
$teamId = 'TeamID8';

$measureType = 'MeasureType8';

$perMode = 'PerMode6';

$plusMinus = 'PlusMinus0';

$paceAdjust = 'PaceAdjust2';

$rank = 'Rank2';

$season = 'Season0';

$seasonType = 'SeasonType8';

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
$apiResponse = $api->teamdashboardbylastngamesGet(
    $teamId,
    $measureType,
    $perMode,
    $plusMinus,
    $paceAdjust,
    $rank,
    $season,
    $seasonType,
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



