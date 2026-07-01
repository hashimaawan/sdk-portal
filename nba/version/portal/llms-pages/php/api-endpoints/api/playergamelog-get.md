# Playergamelog GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmdhbWVsb2dfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function playergamelogGET(string $playerID, string $season, string $seasonType): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `playerID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$playerID = 'PlayerID6';

$season = 'Season0';

$seasonType = 'SeasonType8';

$aPIController = $client->getAPIController();

try {
    $aPIController->playergamelogGET(
        $playerID,
        $season,
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



