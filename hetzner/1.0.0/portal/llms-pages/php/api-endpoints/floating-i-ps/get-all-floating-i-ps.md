# Get All Floating I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGFsbCUyNTIwRmxvYXRpbmclMjUyMElQcw

Returns all Floating IP objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllFloatingIPs(
    ?string $name = null,
    ?string $labelSelector = null,
    ?string $sort = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter Floating IPs by their name. The response will only contain the Floating IP matching the specified name. |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter Floating IPs by labels. The response will only contain Floating IPs matching the label selector. |
| `sort` | [`?string(Sort2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `floating_ips` key in the reply contains an array of Floating IP objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`FloatingIpsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ips-response.md).


# Example Usage

```php
$floatingIPsApi = $client->getFloatingIPsApi();
$apiResponse = $floatingIPsApi->getAllFloatingIPs();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'FloatingIpsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



