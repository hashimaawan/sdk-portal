# Leaguedashptteamdefend GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkxlYWd1ZWRhc2hwdHRlYW1kZWZlbmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function leaguedashptteamdefendGET(
    string $leagueID,
    string $perMode,
    string $season,
    string $seasonType,
    string $defenseCategory
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `defenseCategory` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$perMode = 'PerMode6';

$season = 'Season0';

$seasonType = 'SeasonType8';

$defenseCategory = 'DefenseCategory0';

$aPIController = $client->getAPIController();

try {
    $aPIController->leaguedashptteamdefendGET(
        $leagueID,
        $perMode,
        $season,
        $seasonType,
        $defenseCategory
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



