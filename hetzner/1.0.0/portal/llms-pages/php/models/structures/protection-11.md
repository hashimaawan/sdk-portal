# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network

*This model accepts additional fields of type array.*


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Network from being deleted | getDelete(): bool | setDelete(bool delete): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Protection11Builder;
use HetznerCloudApiLib\ApiHelper;

$protection11 = Protection11Builder::init(
    false
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



