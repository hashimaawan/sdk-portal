# Playercareerstats GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXllcmNhcmVlcnN0YXRzX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function playercareerstatsGET(string $perMode, string $playerID): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perMode` | `string` | Query, Required | - |
| `playerID` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$perMode = 'PerMode6';

$playerID = 'PlayerID6';

$aPIController = $client->getAPIController();

try {
    $aPIController->playercareerstatsGET(
        $perMode,
        $playerID
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



