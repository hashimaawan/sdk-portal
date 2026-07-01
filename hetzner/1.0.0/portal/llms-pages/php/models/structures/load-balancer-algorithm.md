# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`string(Type28)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-28.md) | Required | Type of the algorithm | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerAlgorithmBuilder;
use HetznerCloudApiLib\Models\Type28;
use HetznerCloudApiLib\ApiHelper;

$loadBalancerAlgorithm = LoadBalancerAlgorithmBuilder::init(
    Type28::ROUND_ROBIN
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



