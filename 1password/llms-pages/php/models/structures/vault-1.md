# Vault 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlZhdWx0MQ

*This model accepts additional fields of type array.*


# Class Name

`Vault1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `string` | Required | **Constraints**: *Pattern*: `^[\da-z]{26}$` | getId(): string | setId(string id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\Vault1Builder;
use M1PasswordConnectLib\ApiHelper;

$vault1 = Vault1Builder::init(
    'id0'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



