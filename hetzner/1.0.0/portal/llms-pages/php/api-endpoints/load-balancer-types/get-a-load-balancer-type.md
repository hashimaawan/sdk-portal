# Get a Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXIlMjUyMFR5cGU

Gets a specific Load Balancer type object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getALoadBalancerType(int $id): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Load Balancer type |


# Response Type

**200**: The `load_balancer_type` key in the reply contains a Load Balancer type object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`LoadBalancerTypesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-types-response-1.md).


# Example Usage

```php
$id = 112;

$loadBalancerTypesApi = $client->getLoadBalancerTypesApi();
$apiResponse = $loadBalancerTypesApi->getALoadBalancerType($id);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'LoadBalancerTypesResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



