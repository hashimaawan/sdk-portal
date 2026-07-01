# Homepagev 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkhvbWVwYWdldjJfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function homepagev2Get(
    string $statType,
    string $leagueId,
    string $season,
    string $seasonType,
    string $playerOrTeam,
    string $playerScope,
    string $gameScope,
    ?string $game = null,
    ?string $player = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statType` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerOrTeam` | `string` | Query, Required | - |
| `playerScope` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `game` | `?string` | Query, Optional | - |
| `player` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$statType = 'StatType8';

$leagueId = 'LeagueID4';

$season = 'Season0';

$seasonType = 'SeasonType8';

$playerOrTeam = 'PlayerOrTeam8';

$playerScope = 'PlayerScope2';

$gameScope = 'GameScope0';

$api = $client->getAPI();
$apiResponse = $api->homepagev2Get(
    $statType,
    $leagueId,
    $season,
    $seasonType,
    $playerOrTeam,
    $playerScope,
    $gameScope
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



