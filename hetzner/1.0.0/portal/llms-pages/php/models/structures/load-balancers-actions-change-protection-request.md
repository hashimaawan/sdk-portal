# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Load Balancer from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancersActionsChangeProtectionRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$loadBalancersActionsChangeProtectionRequest = LoadBalancersActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



