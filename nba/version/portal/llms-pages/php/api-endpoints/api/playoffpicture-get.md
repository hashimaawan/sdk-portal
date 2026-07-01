# Playoffpicture GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlBsYXlvZmZwaWN0dXJlX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function playoffpictureGET(string $leagueID, string $seasonID): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `leagueID` | `string` | Query, Required | - |
| `seasonID` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$leagueID = 'LeagueID4';

$seasonID = 'SeasonID6';

$aPIController = $client->getAPIController();

try {
    $aPIController->playoffpictureGET(
        $leagueID,
        $seasonID
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



