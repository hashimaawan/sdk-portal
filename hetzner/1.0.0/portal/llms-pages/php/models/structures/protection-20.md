# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type array.*


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Server from being deleted | getDelete(): bool | setDelete(bool delete): void |
| `rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt | getRebuild(): bool | setRebuild(bool rebuild): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Protection20Builder;
use HetznerCloudApiLib\ApiHelper;

$protection20 = Protection20Builder::init(
    false,
    false
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



