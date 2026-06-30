# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function teaminfocommonGET(string $season, string $teamID, string $leagueID, string $seasonType): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |
| `leagueID` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$season = 'Season0';

$teamID = 'TeamID8';

$leagueID = 'LeagueID4';

$seasonType = 'SeasonType8';

$aPIController = $client->getAPIController();

try {
    $aPIController->teaminfocommonGET(
        $season,
        $teamID,
        $leagueID,
        $seasonType
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



