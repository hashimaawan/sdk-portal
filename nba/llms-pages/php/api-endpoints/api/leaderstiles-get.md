# Leaderstiles GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkxlYWRlcnN0aWxlc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function leaderstilesGET(
    string $stat,
    string $leagueID,
    string $season,
    string $seasonType,
    string $playerOrTeam,
    string $playerScope,
    string $gameScope,
    ?string $game = null,
    ?string $player = null
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stat` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `playerOrTeam` | `string` | Query, Required | - |
| `playerScope` | `string` | Query, Required | - |
| `gameScope` | `string` | Query, Required | - |
| `game` | `?string` | Query, Optional | - |
| `player` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$stat = 'Stat2';

$leagueID = 'LeagueID4';

$season = 'Season0';

$seasonType = 'SeasonType8';

$playerOrTeam = 'PlayerOrTeam8';

$playerScope = 'PlayerScope2';

$gameScope = 'GameScope0';

$aPIController = $client->getAPIController();

try {
    $aPIController->leaderstilesGET(
        $stat,
        $leagueID,
        $season,
        $seasonType,
        $playerOrTeam,
        $playerScope,
        $gameScope
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



