# Get All Locations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYWxsJTI1MjBMb2NhdGlvbnM

Returns all Location objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllLocations(?string $name = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter Locations by their name. The response will only contain the Location matching the specified name. |


# Response Type

**200**: The `locations` key in the reply contains an array of Location objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`LocationsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/locations-response.md).


# Example Usage

```php
$locationsApi = $client->getLocationsApi();
$apiResponse = $locationsApi->getAllLocations();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'LocationsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



