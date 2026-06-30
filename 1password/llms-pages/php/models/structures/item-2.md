# Item 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkl0ZW0y

*This model accepts additional fields of type array.*


# Class Name

`Item2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | getId(): ?string | setId(?string id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\Item2Builder;
use M1PasswordConnectLib\ApiHelper;

$item2 = Item2Builder::init()
    ->id('id2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



