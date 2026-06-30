# Section 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlNlY3Rpb24x

For files that are in a section, this field describes the section.

*This model accepts additional fields of type array.*


# Class Name

`Section1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\Section1Builder;
use M1PasswordConnectLib\ApiHelper;

$section1 = Section1Builder::init()
    ->id('id2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



