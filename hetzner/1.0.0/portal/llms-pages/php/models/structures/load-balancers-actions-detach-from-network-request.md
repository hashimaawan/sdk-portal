# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `network` | `float` | Required | ID of an existing network to detach the Load Balancer from | getNetwork(): float | setNetwork(float network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancersActionsDetachFromNetworkRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$loadBalancersActionsDetachFromNetworkRequest = LoadBalancersActionsDetachFromNetworkRequestBuilder::init(
    4711
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



