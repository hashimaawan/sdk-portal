# Scoreboard GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRlNjb3JlYm9hcmRfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function scoreboardGET(string $gameDate, string $leagueID, string $dayOffset): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameDate` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `dayOffset` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$gameDate = 'GameDate8';

$leagueID = 'LeagueID4';

$dayOffset = 'DayOffset6';

$aPIController = $client->getAPIController();

try {
    $aPIController->scoreboardGET(
        $gameDate,
        $leagueID,
        $dayOffset
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



