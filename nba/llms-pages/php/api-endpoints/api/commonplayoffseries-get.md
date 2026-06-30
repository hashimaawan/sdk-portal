# Commonplayoffseries GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnBsYXlvZmZzZXJpZXNfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function commonplayoffseriesGET(string $leagueID, string $season): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `season` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$season = 'Season0';

$aPIController = $client->getAPIController();

try {
    $aPIController->commonplayoffseriesGET(
        $leagueID,
        $season
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



