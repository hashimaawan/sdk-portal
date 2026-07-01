# Playbyplay GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXlieXBsYXlfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function playbyplayGET(string $gameID, string $startPeriod, string $endPeriod): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `string` | Query, Required | - |
| `startPeriod` | `string` | Query, Required | - |
| `endPeriod` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$gameID = 'GameID8';

$startPeriod = 'StartPeriod4';

$endPeriod = 'EndPeriod0';

$aPIController = $client->getAPIController();

try {
    $aPIController->playbyplayGET(
        $gameID,
        $startPeriod,
        $endPeriod
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



