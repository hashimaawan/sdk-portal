# Common Team Years GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkNvbW1vblRlYW1ZZWFyc19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function commonTeamYearsGET(string $leagueID): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$aPIController = $client->getAPIController();

try {
    $aPIController->commonTeamYearsGET($leagueID);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



