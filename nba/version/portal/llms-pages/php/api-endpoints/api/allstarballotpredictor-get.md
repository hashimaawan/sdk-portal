# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/version/portal/#/php/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```php
function allstarballotpredictorGET(
    string $westPlayer1,
    string $westPlayer2,
    string $westPlayer3,
    string $westPlayer4,
    string $westPlayer5,
    string $eastPlayer1,
    string $eastPlayer2,
    string $eastPlayer3,
    string $eastPlayer4,
    string $eastPlayer5,
    ?string $pointCap = null
): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `westPlayer1` | `string` | Query, Required | - |
| `westPlayer2` | `string` | Query, Required | - |
| `westPlayer3` | `string` | Query, Required | - |
| `westPlayer4` | `string` | Query, Required | - |
| `westPlayer5` | `string` | Query, Required | - |
| `eastPlayer1` | `string` | Query, Required | - |
| `eastPlayer2` | `string` | Query, Required | - |
| `eastPlayer3` | `string` | Query, Required | - |
| `eastPlayer4` | `string` | Query, Required | - |
| `eastPlayer5` | `string` | Query, Required | - |
| `pointCap` | `?string` | Query, Optional | - |


# Response Type

**200**: 200 OK

`void`


# Example Usage

```php
$westPlayer1 = 'WestPlayer10';

$westPlayer2 = 'WestPlayer24';

$westPlayer3 = 'WestPlayer32';

$westPlayer4 = 'WestPlayer48';

$westPlayer5 = 'WestPlayer56';

$eastPlayer1 = 'EastPlayer18';

$eastPlayer2 = 'EastPlayer26';

$eastPlayer3 = 'EastPlayer32';

$eastPlayer4 = 'EastPlayer44';

$eastPlayer5 = 'EastPlayer54';

$aPIController = $client->getAPIController();

try {
    $aPIController->allstarballotpredictorGET(
        $westPlayer1,
        $westPlayer2,
        $westPlayer3,
        $westPlayer4,
        $westPlayer5,
        $eastPlayer1,
        $eastPlayer2,
        $eastPlayer3,
        $eastPlayer4,
        $eastPlayer5
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



