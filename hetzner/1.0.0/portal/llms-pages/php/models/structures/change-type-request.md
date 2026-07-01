# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancerType` | `string` | Required | ID or name of Load Balancer type the Load Balancer should migrate to | getLoadBalancerType(): string | setLoadBalancerType(string loadBalancerType): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ChangeTypeRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$changeTypeRequest = ChangeTypeRequestBuilder::init(
    'lb21'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



