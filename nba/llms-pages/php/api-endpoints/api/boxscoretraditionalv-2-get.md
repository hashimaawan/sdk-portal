# Boxscoretraditionalv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JldHJhZGl0aW9uYWx2Ml9HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function boxscoretraditionalv2GET(
    string $gameID,
    string $startPeriod,
    string $endPeriod,
    string $startRange,
    string $endRange,
    string $rangeType
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `string` | Query, Required | - |
| `startPeriod` | `string` | Query, Required | - |
| `endPeriod` | `string` | Query, Required | - |
| `startRange` | `string` | Query, Required | - |
| `endRange` | `string` | Query, Required | - |
| `rangeType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$gameID = 'GameID8';

$startPeriod = 'StartPeriod4';

$endPeriod = 'EndPeriod0';

$startRange = 'StartRange0';

$endRange = 'EndRange2';

$rangeType = 'RangeType0';

$aPIController = $client->getAPIController();

try {
    $aPIController->boxscoretraditionalv2GET(
        $gameID,
        $startPeriod,
        $endPeriod,
        $startRange,
        $endRange,
        $rangeType
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



