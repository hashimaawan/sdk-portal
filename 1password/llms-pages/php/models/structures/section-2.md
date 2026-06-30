# Section 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlNlY3Rpb24y

*This model accepts additional fields of type array.*


# Class Name

`Section2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `label` | `?string` | Optional | - | getLabel(): ?string | setLabel(?string label): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\Section2Builder;
use M1PasswordConnectLib\ApiHelper;

$section2 = Section2Builder::init()
    ->id('id4')
    ->label('label4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



