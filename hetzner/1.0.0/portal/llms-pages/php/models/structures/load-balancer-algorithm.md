# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`string(Type28Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-28.md) | Required | Type of the algorithm | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerAlgorithmBuilder;
use HetznerCloudAPILib\Models\Type28Enum;

$loadBalancerAlgorithm = LoadBalancerAlgorithmBuilder::init(
    Type28Enum::ROUND_ROBIN
)->build();
```



