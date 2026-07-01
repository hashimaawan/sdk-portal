# Playerdashptshotlog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmRhc2hwdHNob3Rsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function playerdashptshotlogGET(
    ?string $leagueID = null,
    ?string $season = null,
    ?string $seasonType = null,
    ?string $playerID = null,
    ?string $teamID = null
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `?string` | Query, Optional | - |
| `season` | `?string` | Query, Optional | - |
| `seasonType` | `?string` | Query, Optional | - |
| `playerID` | `?string` | Query, Optional | - |
| `teamID` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$aPIController = $client->getAPIController();

try {
    $aPIController->playerdashptshotlogGET();
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



