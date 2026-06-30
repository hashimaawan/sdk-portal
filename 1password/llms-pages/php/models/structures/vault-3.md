# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type array.*


# Class Name

`Vault3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | getId(): ?string | setId(?string id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\Vault3Builder;
use M1PasswordConnectLib\ApiHelper;

$vault3 = Vault3Builder::init()
    ->id('id0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



