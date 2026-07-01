# Shotchartlineupdetail GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlNob3RjaGFydGxpbmV1cGRldGFpbF9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function shotchartlineupdetailGet(
    string $leagueId,
    string $season,
    string $seasonType,
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
    string $lastNGames,
    string $gameId,
    string $groupId,
    string $contextMeasure,
    string $contextFilter
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
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
| `gameId` | `string` | Query, Required | - |
| `groupId` | `string` | Query, Required | - |
| `contextMeasure` | `string` | Query, Required | - |
| `contextFilter` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$leagueId = 'LeagueID4';

$season = 'Season0';

$seasonType = 'SeasonType8';

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

$gameId = 'GameID8';

$groupId = 'GROUP_ID6';

$contextMeasure = 'ContextMeasure2';

$contextFilter = 'ContextFilter6';

$api = $client->getAPI();
$apiResponse = $api->shotchartlineupdetailGet(
    $leagueId,
    $season,
    $seasonType,
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
    $lastNGames,
    $gameId,
    $groupId,
    $contextMeasure,
    $contextFilter
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



