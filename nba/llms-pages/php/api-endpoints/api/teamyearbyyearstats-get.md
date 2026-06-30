# Teamyearbyyearstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRlRlYW15ZWFyYnl5ZWFyc3RhdHNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function teamyearbyyearstatsGET(string $leagueID, string $seasonType, string $perMode, string $teamID): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |
| `perMode` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$seasonType = 'SeasonType8';

$perMode = 'PerMode6';

$teamID = 'TeamID8';

$aPIController = $client->getAPIController();

try {
    $aPIController->teamyearbyyearstatsGET(
        $leagueID,
        $seasonType,
        $perMode,
        $teamID
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



