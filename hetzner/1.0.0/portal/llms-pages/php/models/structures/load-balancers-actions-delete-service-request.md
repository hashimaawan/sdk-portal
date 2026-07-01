# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `listenPort` | `float` | Required | The listen port of the service you want to delete | getListenPort(): float | setListenPort(float listenPort): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancersActionsDeleteServiceRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$loadBalancersActionsDeleteServiceRequest = LoadBalancersActionsDeleteServiceRequestBuilder::init(
    4711
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



