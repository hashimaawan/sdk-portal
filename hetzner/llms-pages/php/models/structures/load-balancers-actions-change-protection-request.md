# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Load Balancer from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersActionsChangeProtectionRequestBuilder;

$loadBalancersActionsChangeProtectionRequest = LoadBalancersActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->build();
```



