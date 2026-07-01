# Commonallplayers GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkNvbW1vbmFsbHBsYXllcnNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function commonallplayersGET(string $leagueID, string $season, string $isOnlyCurrentSeason): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `isOnlyCurrentSeason` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$season = 'Season0';

$isOnlyCurrentSeason = 'IsOnlyCurrentSeason6';

$aPIController = $client->getAPIController();

try {
    $aPIController->commonallplayersGET(
        $leagueID,
        $season,
        $isOnlyCurrentSeason
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



