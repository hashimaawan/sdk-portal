# Get a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Gets a specific Load Balancer object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getALoadBalancer(int $id): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**200**: The `load_balancer` key contains the Load Balancer

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`LoadBalancersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancers-response-2.md).


# Example Usage

```php
$id = 112;

$loadBalancersApi = $client->getLoadBalancersApi();
$apiResponse = $loadBalancersApi->getALoadBalancer($id);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'LoadBalancersResponse2:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



