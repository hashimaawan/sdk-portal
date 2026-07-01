# Get All Load Balancer Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwVHlwZXM

Gets all Load Balancer type objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllLoadBalancerTypes(?string $name = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter Load Balancer types by their name. The response will only contain the Load Balancer type matching the specified name. |


# Response Type

**200**: The `load_balancer_types` key in the reply contains an array of Load Balancer type objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`LoadBalancerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-types-response.md).


# Example Usage

```php
$loadBalancerTypesApi = $client->getLoadBalancerTypesApi();
$apiResponse = $loadBalancerTypesApi->getAllLoadBalancerTypes();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'LoadBalancerTypesResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



