# Get a Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXIlMjUyMFR5cGU

Gets a specific Load Balancer type object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getALoadBalancerType(int $id): LoadBalancerTypesResponse1
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Load Balancer type |


# Response Type

**200**: The `load_balancer_type` key in the reply contains a Load Balancer type object with this structure

[`LoadBalancerTypesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-types-response-1.md)


# Example Usage

```php
$id = 112;

$loadBalancerTypesController = $client->getLoadBalancerTypesController();

try {
    $result = $loadBalancerTypesController->getALoadBalancerType($id);
    echo 'LoadBalancerTypesResponse1:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



