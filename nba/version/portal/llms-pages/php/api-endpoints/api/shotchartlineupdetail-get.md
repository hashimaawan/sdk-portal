# Shotchartlineupdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGxpbmV1cGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function shotchartlineupdetailGET(
    string $leagueID,
    string $season,
    string $seasonType,
    string $teamID,
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
    string $gameID,
    string $gROUPID,
    string $contextMeasure,
    string $contextFilter
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |
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
| `gameID` | `string` | Query, Required | - |
| `gROUPID` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |
| `contextFilter` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$season = 'Season0';

$seasonType = 'SeasonType8';

$teamID = 'TeamID8';

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

$gameID = 'GameID8';

$gROUPID = 'GROUP_ID6';

$contextMeasure = 'ContextMeasure2';

$contextFilter = 'ContextFilter6';

$aPIController = $client->getAPIController();

try {
    $aPIController->shotchartlineupdetailGET(
        $leagueID,
        $season,
        $seasonType,
        $teamID,
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
        $gameID,
        $gROUPID,
        $contextMeasure,
        $contextFilter
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



