# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `network` | `float` | Required | ID of an existing network to detach the Load Balancer from | getNetwork(): float | setNetwork(float network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersActionsDetachFromNetworkRequestBuilder;

$loadBalancersActionsDetachFromNetworkRequest = LoadBalancersActionsDetachFromNetworkRequestBuilder::init(
    4711
)->build();
```



