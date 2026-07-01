# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVzZWRCeQ

*This model accepts additional fields of type array.*


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of resource referenced | getId(): int | setId(int id): void |
| `type` | `string` | Required | Type of resource referenced | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UsedByBuilder;
use HetznerCloudApiLib\ApiHelper;

$usedBy = UsedByBuilder::init(
    4711,
    'load_balancer'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



