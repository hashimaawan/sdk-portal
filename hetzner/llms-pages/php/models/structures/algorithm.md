# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`string(Type28Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-28.md) | Required | Type of the algorithm | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AlgorithmBuilder;
use HetznerCloudAPILib\Models\Type28Enum;

$algorithm = AlgorithmBuilder::init(
    Type28Enum::ROUND_ROBIN
)->build();
```



