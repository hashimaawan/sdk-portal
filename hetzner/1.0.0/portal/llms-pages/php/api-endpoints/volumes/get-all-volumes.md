# Get All Volumes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGFsbCUyNTIwVm9sdW1lcw

Gets all existing Volumes that you have available.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllVolumes(
    ?string $status = null,
    ?string $sort = null,
    ?string $name = null,
    ?string $labelSelector = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`?string(Status23)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Volumes matching the status. |
| `sort` | [`?string(Sort)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `volumes` key contains a list of volumes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`VolumesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/volumes-response.md).


# Example Usage

```php
$volumesApi = $client->getVolumesApi();
$apiResponse = $volumesApi->getAllVolumes();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'VolumesResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



