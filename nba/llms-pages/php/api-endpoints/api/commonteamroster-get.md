# Commonteamroster GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkNvbW1vbnRlYW1yb3N0ZXJfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function commonteamrosterGET(string $season, string $teamID): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Required | - |
| `teamID` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$season = 'Season0';

$teamID = 'TeamID8';

$aPIController = $client->getAPIController();

try {
    $aPIController->commonteamrosterGET(
        $season,
        $teamID
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



