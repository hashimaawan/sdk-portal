# Get All Datacenters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhbGwlMjUyMERhdGFjZW50ZXJz

Returns all Datacenter objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllDatacenters(?string $name = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter Datacenters by their name. The response will only contain the Datacenter matching the specified name. When the name does not match the Datacenter name format, an `invalid_input` error is returned. |


# Response Type

**200**: The reply contains the `datacenters` and `recommendation` keys

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`DatacentersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/datacenters-response.md).


# Example Usage

```php
$datacentersApi = $client->getDatacentersApi();
$apiResponse = $datacentersApi->getAllDatacenters();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'DatacentersResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



