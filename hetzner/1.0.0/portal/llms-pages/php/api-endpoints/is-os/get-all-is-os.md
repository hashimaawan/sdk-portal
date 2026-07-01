# Get All IS Os

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFsbCUyNTIwSVNPcw

Returns all available ISO objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllIsOs(?string $name = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter ISOs by their name. The response will only contain the ISO matching the specified name. |


# Response Type

**200**: The `isos` key in the reply contains an array of iso objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`IsosResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/isos-response.md).


# Example Usage

```php
$isOsApi = $client->getIsOsApi();
$apiResponse = $isOsApi->getAllIsOs();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'IsosResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



