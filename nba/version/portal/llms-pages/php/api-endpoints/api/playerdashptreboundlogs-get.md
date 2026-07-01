# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function playerdashptreboundlogsGET(
    ?string $season = null,
    ?string $seasonType = null,
    ?string $playerID = null,
    ?string $teamID = null,
    ?string $outcome = null,
    ?string $location = null,
    ?string $month = null,
    ?string $seasonSegment = null,
    ?string $dateFrom = null,
    ?string $dateTo = null,
    ?string $opponentTeamID = null,
    ?string $vsConference = null,
    ?string $vsDivision = null,
    ?string $gameSegment = null,
    ?string $period = null,
    ?string $lastNGames = null
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `?string` | Query, Optional | - |
| `seasonType` | `?string` | Query, Optional | - |
| `playerID` | `?string` | Query, Optional | - |
| `teamID` | `?string` | Query, Optional | - |
| `outcome` | `?string` | Query, Optional | - |
| `location` | `?string` | Query, Optional | - |
| `month` | `?string` | Query, Optional | - |
| `seasonSegment` | `?string` | Query, Optional | - |
| `dateFrom` | `?string` | Query, Optional | - |
| `dateTo` | `?string` | Query, Optional | - |
| `opponentTeamID` | `?string` | Query, Optional | - |
| `vsConference` | `?string` | Query, Optional | - |
| `vsDivision` | `?string` | Query, Optional | - |
| `gameSegment` | `?string` | Query, Optional | - |
| `period` | `?string` | Query, Optional | - |
| `lastNGames` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$aPIController = $client->getAPIController();

try {
    $aPIController->playerdashptreboundlogsGET();
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



