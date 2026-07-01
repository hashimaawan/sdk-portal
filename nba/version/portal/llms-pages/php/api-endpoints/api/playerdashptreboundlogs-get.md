# Playerdashptreboundlogs GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHJlYm91bmRsb2dzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function playerdashptreboundlogsGet(
    ?string $season = null,
    ?string $seasonType = null,
    ?string $playerId = null,
    ?string $teamId = null,
    ?string $outcome = null,
    ?string $location = null,
    ?string $month = null,
    ?string $seasonSegment = null,
    ?string $dateFrom = null,
    ?string $dateTo = null,
    ?string $opponentTeamId = null,
    ?string $vsConference = null,
    ?string $vsDivision = null,
    ?string $gameSegment = null,
    ?string $period = null,
    ?string $lastNGames = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `?string` | Query, Optional | - |
| `seasonType` | `?string` | Query, Optional | - |
| `playerId` | `?string` | Query, Optional | - |
| `teamId` | `?string` | Query, Optional | - |
| `outcome` | `?string` | Query, Optional | - |
| `location` | `?string` | Query, Optional | - |
| `month` | `?string` | Query, Optional | - |
| `seasonSegment` | `?string` | Query, Optional | - |
| `dateFrom` | `?string` | Query, Optional | - |
| `dateTo` | `?string` | Query, Optional | - |
| `opponentTeamId` | `?string` | Query, Optional | - |
| `vsConference` | `?string` | Query, Optional | - |
| `vsDivision` | `?string` | Query, Optional | - |
| `gameSegment` | `?string` | Query, Optional | - |
| `period` | `?string` | Query, Optional | - |
| `lastNGames` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$api = $client->getAPI();
$apiResponse = $api->playerdashptreboundlogsGet();

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



