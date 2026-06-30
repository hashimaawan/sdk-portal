# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type array.*


# Class Name

`Url`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `href` | `string` | Required | - | getHref(): string | setHref(string href): void |
| `label` | `?string` | Optional | - | getLabel(): ?string | setLabel(?string label): void |
| `primary` | `?bool` | Optional | - | getPrimary(): ?bool | setPrimary(?bool primary): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\UrlBuilder;
use M1PasswordConnectLib\ApiHelper;

$url = UrlBuilder::init(
    'href6'
)
    ->label('label4')
    ->primary(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



