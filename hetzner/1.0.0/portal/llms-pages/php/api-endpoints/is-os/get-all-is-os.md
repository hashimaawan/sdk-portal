# Get All IS Os

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFsbCUyNTIwSVNPcw

Returns all available ISO objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllISOs(?string $name = null): IsosResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter ISOs by their name. The response will only contain the ISO matching the specified name. |


# Response Type

**200**: The `isos` key in the reply contains an array of iso objects with this structure

[`IsosResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/isos-response.md)


# Example Usage

```php
$iSOsController = $client->getISOsController();

try {
    $result = $iSOsController->getAllISOs();
    echo 'IsosResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



