# Delete a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkRlbGV0ZSUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Deletes a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteALoadBalancer(int $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**204**: Load Balancer deleted

`void`


# Example Usage

```php
$id = 112;

$loadBalancersController = $client->getLoadBalancersController();

try {
    $loadBalancersController->deleteALoadBalancer($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



