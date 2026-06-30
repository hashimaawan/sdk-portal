# Draftcombinenonstationaryshooting GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/php/x-redirect/JTI0ZSUyRiUyRkRyYWZ0Y29tYmluZW5vbnN0YXRpb25hcnlzaG9vdGluZ19HRVQ

:information_source: **Note** This endpoint does not require authentication.

```php
function draftcombinenonstationaryshootingGET(string $leagueID, string $seasonYear): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `seasonYear` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$seasonYear = 'SeasonYear6';

$aPIController = $client->getAPIController();

try {
    $aPIController->draftcombinenonstationaryshootingGET(
        $leagueID,
        $seasonYear
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



