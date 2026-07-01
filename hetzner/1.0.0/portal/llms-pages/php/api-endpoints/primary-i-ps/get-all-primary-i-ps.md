# Get All Primary I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYWxsJTI1MjBQcmltYXJ5JTI1MjBJUHM

Returns all Primary IP objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllPrimaryIPs(
    ?string $name = null,
    ?string $labelSelector = null,
    ?string $ip = null,
    ?string $sort = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `ip` | `?string` | Query, Optional | Can be used to filter resources by their ip. The response will only contain the resources matching the specified ip. |
| `sort` | [`?string(Sort2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `primary_ips` key contains an array of Primary IP objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PrimaryIPsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/primary-i-ps-response.md).


# Example Usage

```php
$ip = '127.0.0.1';

$primaryIPsApi = $client->getPrimaryIPsApi();
$apiResponse = $primaryIPsApi->getAllPrimaryIPs(
    null,
    null,
    $ip
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PrimaryIPsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



