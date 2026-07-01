# Get All Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwVHlwZXMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVyJTI1MjBUeXBlcw

Gets all Server type objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllServerTypes(?string $name = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter Server types by their name. The response will only contain the Server type matching the specified name. |


# Response Type

**200**: The `server_types` key in the reply contains an array of Server type objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ServerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-types-response.md).


# Example Usage

```php
$serverTypesApi = $client->getServerTypesApi();
$apiResponse = $serverTypesApi->getAllServerTypes();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ServerTypesResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



