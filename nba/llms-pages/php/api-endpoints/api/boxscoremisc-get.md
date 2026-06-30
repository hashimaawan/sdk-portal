# Boxscoremisc GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkJveHNjb3JlbWlzY19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function boxscoremiscGET(
    ?string $gameID = null,
    ?string $startPeriod = null,
    ?string $endPeriod = null,
    ?string $startRange = null,
    ?string $endRange = null,
    ?string $rangeType = null
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `?string` | Query, Optional | - |
| `startPeriod` | `?string` | Query, Optional | - |
| `endPeriod` | `?string` | Query, Optional | - |
| `startRange` | `?string` | Query, Optional | - |
| `endRange` | `?string` | Query, Optional | - |
| `rangeType` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$aPIController = $client->getAPIController();

try {
    $aPIController->boxscoremiscGET();
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



