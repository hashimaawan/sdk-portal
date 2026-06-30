# Boxscoresummaryv 2 GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkJveHNjb3Jlc3VtbWFyeXYyX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function boxscoresummaryv2GET(string $gameID): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gameID` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$gameID = 'GameID8';

$aPIController = $client->getAPIController();

try {
    $aPIController->boxscoresummaryv2GET($gameID);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



