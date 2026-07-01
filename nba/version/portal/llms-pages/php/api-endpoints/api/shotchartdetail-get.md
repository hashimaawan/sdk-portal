# Shotchartdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function shotchartdetailGET(
    string $seasonType,
    string $teamID,
    string $playerID,
    string $gameID,
    string $outcome,
    string $location,
    string $month,
    string $seasonSegment,
    string $dateFrom,
    string $dateTo,
    string $opponentTeamID,
    string $vsConference,
    string $vsDivision,
    string $position,
    string $rookieYear,
    string $gameSegment,
    string $period,
    string $lastNGames,
    string $contextMeasure
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `seasonType` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |
| `gameID` | `string` | Query, Required | - |
| `outcome` | `string` | Query, Required | - |
| `location` | `string` | Query, Required | - |
| `month` | `string` | Query, Required | - |
| `seasonSegment` | `string` | Query, Required | - |
| `dateFrom` | `string` | Query, Required | - |
| `dateTo` | `string` | Query, Required | - |
| `opponentTeamID` | `string` | Query, Required | - |
| `vsConference` | `string` | Query, Required | - |
| `vsDivision` | `string` | Query, Required | - |
| `position` | `string` | Query, Required | - |
| `rookieYear` | `string` | Query, Required | - |
| `gameSegment` | `string` | Query, Required | - |
| `period` | `string` | Query, Required | - |
| `lastNGames` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$seasonType = 'SeasonType8';

$teamID = 'TeamID8';

$playerID = 'PlayerID6';

$gameID = 'GameID8';

$outcome = 'Outcome4';

$location = 'Location4';

$month = 'Month0';

$seasonSegment = 'SeasonSegment8';

$dateFrom = 'DateFrom6';

$dateTo = 'DateTo0';

$opponentTeamID = 'OpponentTeamID6';

$vsConference = 'VsConference6';

$vsDivision = 'VsDivision6';

$position = 'Position8';

$rookieYear = 'RookieYear8';

$gameSegment = 'GameSegment6';

$period = 'Period2';

$lastNGames = 'LastNGames4';

$contextMeasure = 'ContextMeasure2';

$aPIController = $client->getAPIController();

try {
    $aPIController->shotchartdetailGET(
        $seasonType,
        $teamID,
        $playerID,
        $gameID,
        $outcome,
        $location,
        $month,
        $seasonSegment,
        $dateFrom,
        $dateTo,
        $opponentTeamID,
        $vsConference,
        $vsDivision,
        $position,
        $rookieYear,
        $gameSegment,
        $period,
        $lastNGames,
        $contextMeasure
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



