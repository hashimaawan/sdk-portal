# Leaguedashplayerclutch GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwbGF5ZXJjbHV0Y2hfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function leaguedashplayerclutchGET(
    string $clutchTime,
    string $aheadBehind,
    string $pointDiff,
    string $gameScope,
    string $playerExperience,
    string $playerPosition,
    string $starterBench,
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
    string $lastNGames
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clutchTime` | `string` | Query, Required | - |
| `aheadBehind` | `string` | Query, Required | - |
| `pointDiff` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `playerExperience` | `string` | Query, Required | - |
| `playerPosition` | `string` | Query, Required | - |
| `starterBench` | `string` | Query, Required | - |
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


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$clutchTime = 'ClutchTime4';

$aheadBehind = 'AheadBehind8';

$pointDiff = 'PointDiff6';

$gameScope = 'GameScope0';

$playerExperience = 'PlayerExperience4';

$playerPosition = 'PlayerPosition8';

$starterBench = 'StarterBench0';

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

$aPIController = $client->getAPIController();

try {
    $aPIController->leaguedashplayerclutchGET(
        $clutchTime,
        $aheadBehind,
        $pointDiff,
        $gameScope,
        $playerExperience,
        $playerPosition,
        $starterBench,
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
        $lastNGames
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



