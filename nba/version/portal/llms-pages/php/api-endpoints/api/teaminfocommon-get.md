# Teaminfocommon GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRlRlYW1pbmZvY29tbW9uX0dFVA

:information_source: **Note** This endpoint does not require authentication.

```php
function teaminfocommonGet(string $season, string $teamId, string $leagueId, string $seasonType): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `season` | `string` | Query, Required | - |
| `teamId` | `string` | Query, Required | - |
| `leagueId` | `string` | Query, Required | - |
| `seasonType` | `string` | Query, Required | - |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$season = 'Season0';

$teamId = 'TeamID8';

$leagueId = 'LeagueID4';

$seasonType = 'SeasonType8';

$api = $client->getAPI();
$apiResponse = $api->teaminfocommonGet(
    $season,
    $teamId,
    $leagueId,
    $seasonType
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiException` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiException` |



