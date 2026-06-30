# Playerprofile GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcnByb2ZpbGVfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function playerprofileGET(
    string $leagueID,
    string $playerID,
    string $season,
    string $seasonType,
    string $graphStartSeason,
    string $graphEndSeason,
    string $graphStat
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `graphStartSeason` | `string` | Query, Required | - |
| `graphEndSeason` | `string` | Query, Required | - |
| `graphStat` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$playerID = 'PlayerID6';

$season = 'Season0';

$seasonType = 'SeasonType8';

$graphStartSeason = 'GraphStartSeason2';

$graphEndSeason = 'GraphEndSeason6';

$graphStat = 'GraphStat0';

$aPIController = $client->getAPIController();

try {
    $aPIController->playerprofileGET(
        $leagueID,
        $playerID,
        $season,
        $seasonType,
        $graphStartSeason,
        $graphEndSeason,
        $graphStat
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



