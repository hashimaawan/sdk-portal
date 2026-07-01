# Leaguedashteamshotlocations GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2h0ZWFtc2hvdGxvY2F0aW9uc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function leaguedashteamshotlocationsGET(
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
    string $opponentTeamID,
    string $vsConference,
    string $vsDivision,
    string $gameSegment,
    string $period,
    string $lastNGames,
    string $distanceRange,
    string $gameScope,
    string $playerExperience,
    string $playerPosition,
    string $starterBench
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
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
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |
| `distanceRange` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `playerExperience` | `string` | Query, Required | - |
| `playerPosition` | `string` | Query, Required | - |
| `starterBench` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
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

$opponentTeamID = 'OpponentTeamID6';

$vsConference = 'VsConference6';

$vsDivision = 'VsDivision6';

$gameSegment = 'GameSegment6';

$period = 'Period2';

$lastNGames = 'LastNGames4';

$distanceRange = 'DistanceRange6';

$gameScope = 'GameScope0';

$playerExperience = 'PlayerExperience4';

$playerPosition = 'PlayerPosition8';

$starterBench = 'StarterBench0';

$aPIController = $client->getAPIController();

try {
    $aPIController->leaguedashteamshotlocationsGET(
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
        $opponentTeamID,
        $vsConference,
        $vsDivision,
        $gameSegment,
        $period,
        $lastNGames,
        $distanceRange,
        $gameScope,
        $playerExperience,
        $playerPosition,
        $starterBench
    );
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



